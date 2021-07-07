<template>
  <v-main grid-list-xs>
    <h1>Example</h1>
    <section id="user-input">
      <v-card-text>
        <p>Experience the code below:</p>
        <code
          >&lt;img src&equals;x
          onerror&equals;&quot;alert&lpar;123&rpar;&quot;&gt;</code
        >
      </v-card-text>
      <br>
      <v-form>
        <div class="form-control">
          <v-text-field
            name="user-message"
            label="message"
            for="user-message"
            id="user-message-input"
          ></v-text-field>
        </div>

        <div class="form-control">
          <v-text-field
            name="message-image"
            label="message-image"
            for="message-image"
            id="message-image"
          ></v-text-field>
        </div>

        <button>
          <v-btn block color="primary" type="submit" dark>Send Message</v-btn>
        </button>
      </v-form>
    </section>

    <!-- Where rendered messages will appear: -->
    <section id="user-messages">
      <ul></ul>
    </section>
  </v-main>
</template>

<script>
export default {
  name: 'XSSReflected',

  data () {
    return {
      userMessages: []
    }
  },

  methods: {
    formSubmitHandler (event) {
      event.preventDefault()
      const userMessageInput = event.target.querySelector('#user-message-input')
      const messageImageInput = event.target.querySelector('#message-image')
      const userMessage = userMessageInput.value
      const imageUrl = messageImageInput.value

      if (
        !userMessage ||
        !imageUrl ||
        userMessage.trim().length === 0 ||
        imageUrl.trim().length === 0
      ) {
        alert('Please insert a valid message and image.')
        return
      }

      this.userMessages.push({
        text: userMessage,
        image: imageUrl,
      })

      userMessageInput.value = ''
      messageImageInput.value = ''

      this.renderMessages()
    },

    renderMessages () {
      let messageItems = ''
      for (const message of this.userMessages) {
        messageItems = `
      ${messageItems}
      <li class="message-item">
        <div class="message-image">
          <img src="${message.image}" alt="${message.text}">
        </div>
        <p>${message.text}</p>
      </li>
    `
      }

      const userMessagesList = document.querySelector('ul')
      userMessagesList.innerHTML = messageItems
    },
    bindFormSubmitHandler () {
      const userMessageForm = document.querySelector('form');
      userMessageForm.addEventListener('submit', this.formSubmitHandler)
    }
  },

  mounted () {
    this.bindFormSubmitHandler()
  }
}
</script>

<style lang="scss" scoped>
</style>
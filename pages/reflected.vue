<template>
  <v-card>
    <v-card-text>
      <v-card class="logo py-4 d-flex justify-center">
        <v-card-title class="headline">
          <strong>Reflected XSS</strong>
        </v-card-title>
      </v-card>
      <section id="explain" align="justify">
        <v-card-text>
          [...] XSS attacks can generally be categorized into two categories:
          stored and reflected. There is a third, much less well-known type of
          XSS attack called DOM Based XSS that is discussed separately here []
        </v-card-text>

        <div id="sources">
          <strong>Sources: </strong>
          <a
            href="https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/11-Client_Side_Testing/01-Testing_for_DOM-based_Cross_Site_Scripting.html"
            >owasp</a
          >
        </div>
        <!-- Inspect the component to understand. -->
        <XSSReflected />
      </section>
    </v-card-text>
  </v-card>
</template>

<style lang="scss" scoped>
input {
  border: 1px solid grey;

  &:hover {
    background-color: pink;
    border: 1px solid pink;
  }
}
</style>
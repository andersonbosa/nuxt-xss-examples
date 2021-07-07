<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-text>
          <v-card class="hackerman logo py-4 d-flex justify-start">
            <v-card-title class="headline">
              <strong>❌SS</strong>
            </v-card-title>
          </v-card>
          <section align="justify">
            <br />
            Cross-site scripting (also known as XSS) is a
            <strong>web security vulnerability</strong> that allows an attacker
            to compromise the interactions (e.g., forms, clicks) that users have
            with a vulnerable application. It allows an attacker to circumvent
            the same origin policy, which is designed to segregate different
            websites from each other. Cross-site scripting vulnerabilities
            normally allow an attacker to masquerade as a victim user, to carry
            out any actions that the user is able to perform, and to access any
            of the user's data. If the victim user has privileged access within
            the application, then the attacker might be able to gain full
            control over all of the application's functionality and data. [...]
            <div>
              <br />
              <br />
              <strong>Sources: </strong>
              <a href="https://owasp.org/www-community/attacks/xss/">owasp</a>,
              <a
                href="https://portswigger.net/web-security/cross-site-scripting"
                >portswigger</a
              >
            </div>
          </section>
        </v-card-text>

        <v-card-title primary-title> Examples: </v-card-title>

        <v-card-actions>
          <v-btn color="primary" nuxt to="/reflected"> Reflected </v-btn>
          <v-btn disabled color="primary" nuxt to="/dom-based">
            Dom Based
          </v-btn>
          <v-btn disabled color="primary" nuxt to="#"> Self </v-btn>
          <v-btn disabled color="primary" nuxt to="#"> Blind </v-btn>
          <v-btn disabled color="primary" nuxt to="#"> Persistent </v-btn>
        </v-card-actions>
        <br />
      </v-card>
    </v-col>
  </v-row>
</template>
<style lang="scss" scoped>
.hackerman {
  background-image: url("https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia3.giphy.com%2Fmedia%2FRyXVu4ZW454IM%2Fgiphy.gif&f=1&nofb=1");
  color: white;
}
</style>
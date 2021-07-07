<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-text>
          <v-card class="logo py-4 d-flex justify-center">
            <v-card-title class="headline">
              <strong>DOM Based XSS</strong>
            </v-card-title>
          </v-card>
          <section id="explain" align="justify">
            <br />
            [...] The consequences of DOM-based XSS flaws are as wide ranging as
            those seen in more well known forms of XSS, including cookie
            retrieval, further malicious script injection, etc., and should
            therefore be treated with the same severity. [...]

            <div>
              <br />
              <strong>Sources: </strong>
              <a
                href="https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/11-Client_Side_Testing/01-Testing_for_DOM-based_Cross_Site_Scripting.html"
                >owasp</a
              >
            </div>

          </section>

          <br />
          <br />
          <section id="example"></section>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

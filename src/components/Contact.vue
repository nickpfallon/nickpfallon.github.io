<template id="">
  <div>
    <v-app>
      <div class="main">
        <div class="main-container">
          <h1>contact me</h1>
        </div>
        <div class="contact-info">
          <div>
            <p><v-icon>fa-github</v-icon><span>https://github.com/nickpfallon</span></p>
            <p><v-icon>fa-linkedin</v-icon><span>https://www.linkedin.com/in/nickpfallon/</span></p>
            <p><v-icon>fa-envelope-o</v-icon><span>nickfallonwastaken@gmail.com</span></p>
          </div>
        </div>
      </div>
    </v-app>
  </div>
</template>

<script type="text/javascript">

</script>

<style media="screen">
  .main {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .main-container {
    margin-left: 3em;
    display: flex;
    justify-content: center;
  }
  h1 {
    color: #006064;
    font-size: 4em;
    margin-top: -1em;
    margin-bottom: .75em;
  }
  span {
    margin-left: 1em;
  }
  .contact-info {
    font-size: 1.5em;
    margin-left: 3em;
    display: flex;
    justify-content: center;
  }
</style>

<template id="">
  <div id="about">
    <v-app>
      <div class="container">
        <div class="main-container">
          <h1>about me</h1>
          <section>
            <p>My name is Nick Fallon, and I'm a full stack software developer.  I studied Quantitative Economics and got a minor in Math from CU Boulder in 2015. I worked in restaurants during high school and college. After college, I realized I didn't want to work in a financial discipline and started studying software development.</p>

            <p>I completed the Galvanize Web Development Immersive program in Denver, CO, because I wanted to accelerate my learning and gain the skills to work as a front-end, back-end, or full stack web developer. I love software development because it allows me to use my creativity in a technical way.  I am passionate about math and art and hope to find interesting ways to combine the two in the future.</p>
          </section>
          <h3>skills</h3>
          <div class="text-xs-center skill-container">
            <v-chip v-for="skill in skills" :key="skill.title">
              <v-avatar class="cyan darken-4">{{ skill.letter }}</v-avatar>
              {{ skill.title }}
            </v-chip>
          </div>
        </div>
      </div>
    </v-app>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'about',
  data () {
    return {
      skills: [
        { title: 'JavaScript', letter: 'J' },
        { title: 'CSS3', letter: 'C' },
        { title: 'HTML5', letter: 'H' },
        { title: 'Node.js', letter: 'N' },
        { title: 'jQuery', letter: 'J' },
        { title: 'Vue.js', letter: 'V' },
        { title: 'PostgreSQL', letter: 'P' },
        { title: 'Express', letter: 'E' },
        { title: 'Knex', letter: 'K' },
        { title: 'AJAX', letter: 'A' },
        { title: 'Mocha', letter: 'M' },
        { title: 'Bootstrap', letter: 'B' },
        { title: 'Materialize', letter: 'M' },
        { title: 'Handlebars', letter: 'H' },
        { title: 'React Native', letter: 'R' },
        { title: 'AngularJS 1.x', letter: 'A' },
        { title: 'REST', letter: 'R' },
        { title: 'Git + GitHub', letter: 'G' },
      ]
    }
  }
}

</script>

<style media="screen" scoped>
  .main-container {
    margin-left: 4em;
    margin-right: 4em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  h1 {
    color: #006064;
    font-size: 4em;
    margin-top: 1em;
  }
  section {
    margin-top: 1.25em;
    margin-bottom: 1.25em;
    font-size: 1.25em;
  }
  h3 {
    color: #006064;
    margin-bottom: .75em;
  }
</style>

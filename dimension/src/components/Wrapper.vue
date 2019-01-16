<template>
  <div id="wrapper">
    <header id="header">
      <Logo />
      <div id="content">
        <div class="inn">
          <h1>{{msg}}</h1>
          <div>
            A fully responsive site template designed by HTML5 UP and released for free under the Creative Commons license.
          </div>
        </div>
      </div>
      <nav>
        A
      </nav>
    </header>
  </div>
</template>

<script>
import Logo from './Logo.vue';

export default {
  props: ['msg'],
  components: {
    Logo
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');
@mixin bar-accent {
  content: '';
  display: block;
  position: absolute;
  left: calc(50% - 1px);
  width: 1px;
  height: calc(3.5rem + 1px);
  background: #fff;
}

#wrapper {
  z-index: 3;
  position: relative;
  left: 25%;
  width: 50%;
  top: 10vh;

  &::before {
    content: '';
    display: block;
  }
}

#header {
  align-items: center;
  display: flex;
  flex-direction: column;
  text-align: center;
  > * {
    margin-top: 3.5rem;
    position: relative;

    &::before {
      @include bar-accent;
      color: #fff;
      top: calc(-3.5rem - 1px);
    }

    &:first-child {
      margin-top: 0;
      &:before {
        display: none;
      }
    }
  }
}

.inn {
  color: #ffffff;
  font: {
    family: 'Source Sans Pro', sans-serif;
    weight: 600;
  }
  h1 {
    font: {
      size: 2.25
    }
  }
  div {
    letter-spacing: 0.2rem;
    font-size: 0.8rem;
    line-height: 2;
    font-weight: 100;
  }

  letter-spacing: 0.5rem;
  text-transform: uppercase;
  padding: 3rem 2rem;
  border: {
    top: 1px solid white;
    bottom: 1px solid white;
  }
} 
</style>

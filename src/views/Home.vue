<template>
  <div id="home">
    <div class='norm'>
      <Nav></Nav>
      <Head>
      </Head>
      <br>
      <br>
      <Form style='margin: auto'/>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
    </div>
    <div class='popup' :class='{active: !norm}'>
      <div style='margin: auto'>
        <img src="../assets/fools.png" alt="fools">
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Form from '@/components/Form.vue'
import Head from '@/components/Head.vue'
import Nav from '@/components/Nav.vue'

export default {
  name: 'home',
  components: {
    Nav,
    Form,
    Head
  },
  data() {
    return {
      norm: true
    }
  },
  mounted() {
    setTimeout(() => {
      this.norm = false;
    }, 8000);
  }
}
</script>

<style lang="scss" scoped>
#home {
  margin: auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.ads {
  max-width: 400px;
}
.popup {
  top: 0;
  position: fixed;
  background-color: #1c1c1ce8;
  width: 100%;
  display: flex;
  transition-property: all;
	transition-duration: .5s;
	transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  transform: translateY(-100vh);
  height: 100vh;
  &.active {
    transform: translateY(0);

  }
}

</style>

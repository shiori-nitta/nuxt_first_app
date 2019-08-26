<template>
  <section class="container">
    <h1>{{ title }}</h1>
    <p>{{ $store.state.message }}</p>
    <hr>
    <div class="link"
         @click="$store.commit('count')"
         @click.alt="$store.commit('reset')">
      <a @click="$store.commit('reset')">
        clicked: {{ $store.state.counter }}
      </a>
    </div>
    <router-link to="/other">Go to Other</router-link>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'Hello',
      message: 'this is message.'
    };
  }
}
</script>

<style>
.container {
  padding: 5px 10px;
}

h1 {
  font-size: 60px;
  color: #345980;
}

p {
  padding-top: 5px;
  font-size: 20px;
}

pre {
  padding: 10px;
  font-size: 18px;
  background-color: #efefef;
}

hr {
  margin: 10px 0;
}

a {
  font-size: 16px;
}

.link {
  background: #def;
  padding: 10px;
}
</style>

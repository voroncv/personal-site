<template>
  <div id="app">
    <!-- Sidebar Menu -->
<div class="ui vertical inverted sidebar menu">
  <router-link  class="item" to="/" exact active-class="active">Home</router-link>
  <router-link  class="item" to="/work" exact active-class="active">Work</router-link>
  <router-link  class="item" to="/contacts" exact active-class="active">Contacts</router-link>
</div>


<!-- Page Contents -->
<div class="pusher">
  <div class="ui inverted vertical masthead center aligned segment">

    <div class="ui container">
      <div class="ui large secondary inverted pointing menu">
        <a class="toc item">
          <i class="sidebar icon"></i>
        </a>
        <router-link  class="item" to="/" exact active-class="active">Home</router-link>
        <router-link  class="item" to="/work" exact active-class="active">Work</router-link>
        <router-link  class="item" to="/contacts" exact active-class="active">Contacts</router-link>
      </div>
    </div>

    <div class="ui text container">
      <h1 class="ui inverted header">Alexandr Voroncov</h1>
      <h2>Senior Front-End developer</h2>
    </div>
  </div>

  <router-view></router-view>


  <div class="ui inverted vertical footer segment">
    <div class="ui center aligned container">
      <div class="ui horizontal inverted small divided link list">
        <router-link  class="item" to="/" exact>Home</router-link>
        <router-link  class="item" to="/work" exact>Work</router-link>
        <router-link  class="item" to="/contacts" exact>Contacts</router-link>
      </div>
    </div>
  </div>
</div>
  </div>
</template>

<script>

export default {
  name: 'app'
}
</script>
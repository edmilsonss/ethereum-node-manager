<template>
  <div id="app">
    <div id="nav">
      <nav class="navbar navbar-expand-md navbar-dark bg-dark">
        <div class="container"> <button class="navbar-toggler navbar-toggler-right border-0" type="button" data-toggle="collapse" data-target="#navbar6">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbar6"> <a class="navbar-brand text-primary d-none d-md-block" href="#">
              <i class="fa d-inline fa-lg fa-cube"></i>
              <b> NEoLaBZ</b>
            </a>
            <ul class="navbar-nav mx-auto">
              <li class="nav-item"> <router-link to="/contract-info" class="nav-link" >Contract Info</router-link> </li>
              <li class="nav-item"> <router-link to="/node-info" class="nav-link" >Node Info</router-link> </li>
              <li class="nav-item"> <router-link to="/transact" class="nav-link" >Transact</router-link> </li>
              <li class="nav-item"> <router-link to="/balances" class="nav-link" >Balances</router-link> </li>
            </ul>
            <ul class="navbar-nav">
              <li class="nav-item"> <router-link to="/login" class="nav-link" >Log in</router-link> </li>
              <li class="nav-item"> <router-link to="/about" class="nav-link" >Register</router-link> </li>
            </ul>
          </div>
        </div>
      </nav>
        </div>
    <div id="workspace">
        <router-view/>
    </div>
  </div>

</template>

<style>
  @import './assets/theme.module.css';
</style>

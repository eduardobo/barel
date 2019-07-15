<template>
  <div id="app">
      <b-navbar b-navbar toggleable="lg" type="dark" variant="success">
        <b-container>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
          <b-navbar-brand :to="{name:'home'}">Barel</b-navbar-brand>

          <b-collapse is-nav id="nav-collapse">
            <b-navbar-nav>
              <b-nav-item :to="{name:'product'}" exact>Productos</b-nav-item>
            </b-navbar-nav>

            <b-navbar-nav class="ml-auto">
              <b-nav-item :to="{name:'contact'}">Contacto</b-nav-item>

            </b-navbar-nav>
          </b-collapse>
        </b-container>
      </b-navbar>
      
    <b-container>
      <router-view/>
    </b-container>
    
  </div>
</template>

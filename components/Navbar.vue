<template>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-brand href="#"
        ><b-img height="30" width="120" src="/logo2.png"></b-img
      ></b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item
            v-for="(link, i) in navbarLinks"
            :key="i"
            class="px-2"
            href="#"
            :to="link.to"
            >{{ link.name }}</b-nav-item
          >
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown right>
            <template #button-content>
              <b-avatar></b-avatar>
            </template>
            <b-dropdown-item href="#">Sair</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
</template>

<script>
export default {
  data() {
    return {
      navbarLinks: [
        {
          name: 'Marcas',
          to: '/marcas',
        },
        {
          name: 'Categorias',
          to: '/categorias',
        },
        {
          name: 'Super Tags',
          to: '/marcas',
        },
        {
          name: 'Notebooks',
          to: '/marcas',
        },
        {
          name: 'Partes',
          to: '/marcas',
        },
        {
          name: 'Tags',
          to: '/marcas',
        },
        {
          name: 'Lojas',
          to: '/marcas',
        },
        {
          name: 'Configurações',
          to: '/marcas',
        },
      ],
    }
  },
}
</script>

<style>
</style>
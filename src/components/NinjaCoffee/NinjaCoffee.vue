<template>
  <!-- <p class="is-size-1 has-text-centered">Ninja Coffee</p>
  <p class="is-size-7 has-text-right">Ninja Coffee</p>
  <p class="has-text-weight-bold">Ninja Coffee</p>
  <p class="is-italic">Ninja Coffee</p>
  <p class="is-uppercase has-text-primary">Ninja Coffee</p>
  <p class="title">Title</p>

  <p class="py-1 my-4">Hello Bulma</p>
  <p class="py-6">Hello Bulma</p>
  <p class="px-1 mx-5">Hello Bulma</p>
  <p class="py-1">Hello Bulma</p>

  <section class="section">
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit, obcaecati molestiae! Molestias modi sit facilis reprehenderit obcaecati. Numquam impedit at mollitia, consequatur facere dolorum molestiae rem deleniti quidem maiores odit.</p>
  </section>

  <div class="section">
    <div class="container">
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit, obcaecati molestiae! Molestias modi sit facilis reprehenderit obcaecati. Numquam impedit at mollitia, consequatur facere dolorum molestiae rem deleniti quidem maiores odit.</p>
    </div>
  </div> -->
  <nav class="navbar has-shadow is-white">
    <div class="navbar-brand">
      <a class="navbar-item">
        <img src="../../assets/logo2.png" alt="site logo" style="max-height: 70px" class="py-2 px-2">
      </a>
      <a class="navbar-burger" @click="setNavbarMenuActive">
        <span></span>
        <span></span>
        <span></span>
      </a>
    </div>

    <div class="navbar-menu" v-bind:class="{ 'is-active': isNavbarMenuActive}" id="nav-links">
      <div class="navbar-end">
        <a class="navbar-item">My Account</a>
        <a class="navbar-item">Shopping Cart(0)</a>
      </div>
    </div>
  </nav>

  <!--BreadCrumbs-->
  <div class="section pt-4 pb-0">
    <nav class="breadcrumb has-arrow-separator">
      <ul class="container">
        <li><a class="has-text-grey">Coffee Ninja</a></li>
        <li><a class="has-text-grey">Shop</a></li>
        <li><a class="is-active">Docker Dark Roast</a></li>
      </ul>
    </nav>
  </div>

  <!-- Product Info -->
  <section class="section">
    <div class="container">
      <div class="columns is-vcentered">
        <div class="column is-3">
          <h1 class="is-size-1 title">Docker</h1>
          <h2 class="is-size-2 subtitle">Dark Roast</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum fugiat odit voluptates molestias aut ullam, modi ratione recusandae asperiores nesciunt?</p>
        </div>
        <div class="column is-5 has-text-centered">
          <img src="../../assets/product.png" class="px-6" alt="docker coffee image">
        </div>
        <div class="column is-4">
          <div class="is-size-4 mb-4">$10.95</div>
          <p class="mb-4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Odio, natus!</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'NinjaCoffee',
  data() {
    return {
      isNavbarMenuActive: false
    }
  },
  methods: {
    setNavbarMenuActive() {
      this.isNavbarMenuActive = !this.isNavbarMenuActive
    }
  }

}
</script>

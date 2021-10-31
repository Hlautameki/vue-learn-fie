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
      <div class="columns is-vcentered is-multiline">
        <div class="column is-3-desktop is-6-tablet">
          <h1 class="is-size-3-mobile is-size-1-desktop title">Docker</h1>
          <h2 class="is-size-3-mobile is-size-2-desktop subtitle">Dark Roast</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum fugiat odit voluptates molestias aut ullam, modi ratione recusandae asperiores nesciunt?</p>
        </div>
        <div class="column is-5-desktop is-6-tablet has-text-centered">
          <img src="../../assets/product.png" class="px-6" alt="docker coffee image">
        </div>
        <div class="column is-4-desktop is-12-tablet">
          <div class="is-size-4 mb-4">$10.95</div>
          <p class="mb-4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Odio, natus!</p>
        </div>
      </div>
    </div>
  </section>

  <section class="section">
    <div class="container">
      <div class="columns is-8 is-variable">
        <div class="column is-7-tablet">
          <!-- Tabbed content -->
          <div class="tabs is-boxed">
            <ul>
              <li :class="{ 'is-active': isProductDetailsTabActive}"
                @click="handleTabClick">
                <a>Product Details</a>
              </li>
              <li :class="{ 'is-active': !isProductDetailsTabActive}"
                @click="handleTabClick">
                <a>Delivery Information</a>
              </li>
            </ul>
          </div>
          <div class="px-2">
            <div v-show="isProductDetailsTabActive">
              <h3 class="is-size-5 title">Product Details</h3>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente praesentium hic voluptates, distinctio at optio ratione. Impedit velit, voluptates quia tempora maxime possimus minima magni, pariatur fuga, quasi atque. Minima?</p>
            </div>
            <div v-show="!isProductDetailsTabActive">
              <h3 class="is-size-5 title">Delivery Information</h3>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente praesentium hic voluptates, distinctio at optio ratione. Impedit velit, voluptates quia tempora maxime possimus minima magni, pariatur fuga, quasi atque. Minima?</p>
            </div>
          </div>
        </div>
        <div class="column is-5-tablet">
          <!-- message box -->
          <div class="message">
            <div class="message-header">
              <p>Ern Points with the Coffee Club</p>
            </div>
            <div class="message-body">
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia sunt in libero quasi quidem laudantium! Illo repudiandae facere rerum iure, ipsum dicta a eligendi explicabo veritatis quisquam! Ex, tempora saepe!</p>
            </div>
          </div>
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
      isNavbarMenuActive: false,
      isProductDetailsTabActive: true
    }
  },
  methods: {
    setNavbarMenuActive() {
      this.isNavbarMenuActive = !this.isNavbarMenuActive
    },
    handleTabClick() {
      this.isProductDetailsTabActive = !this.isProductDetailsTabActive
    }
  }

}
</script>

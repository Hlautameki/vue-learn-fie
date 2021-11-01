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
          <form>
            <div class="field">
              <control class="control mb-6">
                <div class="select is-dark">
                  <select>
                    <option>Small (250g)</option>
                    <option>Large (500g)</option>
                  </select>
                </div>
              </control>
            </div>
            <button class="button is-primary">Add to Cart</button>
          </form>
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
            <div class="has-text-centered">
              <button class="button mb-5" @click="isModalActive = true">Sign Up</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Cards -->
  <section class="section is-hidden-mobile">
    <div class="container">
      <h3 class="title has-text-centered is-size-4">Related Products</h3>
      <div class="columns mt-5 is-8 is-variable is-centered">
        <div class="column is-4-tablet is-3-desktop">
          <div class="card">
            <div class="card-image has-text-centered px-6">
              <img src="../../assets/p1.png" alt="product ">
            </div>
            <div class="card-content">
              <p>$12.95</p>
              <p class="title is-size-5">Cortadro Cup</p>
            </div>
            <footer class="card-footer">
              <p class="card-footer-item">
                <a href="" class="has-text-grey">View</a>
              </p>
            </footer>
          </div>
        </div>
        <div class="column is-4-tablet is-3-desktop">
          <div class="card">
            <div class="card-image has-text-centered px-6">
              <img src="../../assets/p2.png" alt="product ">
            </div>
            <div class="card-content">
              <p>$12.95</p>
              <p class="title is-size-5">Docker Light</p>
            </div>
            <footer class="card-footer">
              <p class="card-footer-item">
                <a href="" class="has-text-grey">View</a>
              </p>
            </footer>
          </div>
        </div>
        <div class="column is-4-tablet is-3-desktop">
          <div class="card">
            <div class="card-image has-text-centered px-6">
              <img src="../../assets/p3.png" alt="product ">
            </div>
            <div class="card-content">
              <p>$12.95</p>
              <p class="title is-size-5">Coffee Crush</p>
            </div>
            <footer class="card-footer">
              <p class="card-footer-item">
                <a href="" class="has-text-grey">View</a>
              </p>
            </footer>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- modal -->
  <div class="modal" :class="{ 'is-active' : isModalActive}">
    <div class="modal-background" @click="isModalActive = false"></div>
    <div class="modal-content has-background-white px-5 py-5">
      <h3 class="title mb-6">Join the Club</h3>
      <form class="form">
        <div class="field">
          <label class="label">Name</label>
          <div class="control">
            <input type="text" class="input" placeholder="Name">
          </div>
        </div>
        <div class="field">
          <label class="label">Email</label>
          <div class="control">
            <input type="text" class="input" placeholder="Email">
          </div>
        </div>
        <div class="field">
          <div class="control">
            <label class="checkbox">
              <input type="checkbox">
              I agree to the <a href="">terms & conditions</a>
            </label>
          </div>
        </div>
        <div class="mt-6 has-text-centered">
          <button class="button is-warning">Sign Up</button>
        </div>
      </form>
    </div>
  </div>
  <!-- Footer -->
  <footer class="footer">
    <div class="content has-text-centered">
      <p>Copyright 2020 Coffee Ninja</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'NinjaCoffee',
  data() {
    return {
      isNavbarMenuActive: false,
      isProductDetailsTabActive: true,
      isModalActive: false
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

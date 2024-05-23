<template>
  <q-layout view="hHh lpR fFf">

<!-- Membuat Navbar -->
    <q-header elevated class="bg-yellow text-black">
        <q-toolbar class="justify-center bg-yellow text-black">
          <q-toolbar-title>
            <q-avatar>
              <img src="./assets/coverbento.jpg">
                </q-avatar>
                bento cake
          </q-toolbar-title>
<!-- Navigation Tabs -->
        <div class="flex flex-center flex-auto">
          <q-tabs dense v-model="activeTab">
          <q-tab name="home" @click="navigateTo('home')" class="text-lowercase">home</q-tab>
          <q-tab name="product" @click="navigateTo('product')" class="text-lowercase">product</q-tab>
          <q-tab name="contact" @click="navigateTo('contact')" class="text-lowercase">contact</q-tab>
          <q-tab name="review" @click="navigateTo('review')" class="text-lowercase">review</q-tab>
          <q-tab name="about" @click="navigateTo('about')" class="text-lowercase">about us</q-tab>
          </q-tabs>
        </div>
        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
        </q-toolbar>
    </q-header>
<!-- Left Drawer -->
  <q-drawer v-model="rightDrawerOpen" side="left" overlay>
<!-- drawer content -->
    <q-list>
      <q-item clickable v-ripple>
        <q-item-section>types of bento cakes available:</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>taro cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>sponge cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>bolu coklat</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>cheese cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>roll cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>brownies</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>butter cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>chiffon cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>tiramisu cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>red velvet cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>lemon cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>matcha cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>coffe cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>strawberry cake</q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>blueberry cake</q-item-section>
      </q-item>
    </q-list>
  </q-drawer>
<!-- Page Container -->
    <q-page-container>
      <q-page class="q-pa-md">
<!-- Membuat Carousel -->
        <q-carousel
          animated
          v-model="slide"
          arrows
          navigation
          infinite
          autoplay
          class="carousel-height"
        >
          <q-carousel-slide :name="12" img-src="./assets/bento12.jpg" />  
          <q-carousel-slide :name="1" img-src="./assets/bento1.jpg" />
          <q-carousel-slide :name="2" img-src="./assets/bento2.jpg" />
          <q-carousel-slide :name="3" img-src="./assets/bento3.jpg" />
          <q-carousel-slide :name="4" img-src="./assets/bento4.jpg" />
          <q-carousel-slide :name="5" img-src="./assets/bento5.jpg" />
        </q-carousel>

        <div class="container">
          <p class="paragraf1">Bento cakes are mini tart cakes layered with sweet, colorful cream and various beautiful decorations 
            on top. In terms of how it is made, there are 3 types of cake that are best known, namely sponge cake, butter cake 
            and chiffon cake. Come on, see the explanation of each of the three types of cake below.</p>
          <p class="paragraf2">This can be seen since the arrival of a new trend in the culinary world, especially birthday cakes, 
            namely bento cake. It is called bento cake because this cake is served in a small container or lunch box which we usually 
            call bento. The appearance of this birthday cake looks more attractive and aesthetic.</p>
        </div>

<!-- Membuat Card -->
        <div class="q-gutter-md q-mt-md row justify-around">
          <q-card class="my-card">
            <q-img src="./assets/bento1.jpg" />
            <q-card-section>
              <div class="text-h6">pikachu character</div>
              <div class="text-subtitle1">$99.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento2.jpg" />
            <q-card-section>
              <div class="text-h6">flower character</div>
              <div class="text-subtitle1">$85.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento3.jpg" />
            <q-card-section>
              <div class="text-h6">rainbow character</div>
              <div class="text-subtitle1">$70.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento4.jpg" />
            <q-card-section>
              <div class="text-h6">cloud character</div>
              <div class="text-subtitle1">$90.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento5.jpg" />
            <q-card-section>
              <div class="text-h6">person's character</div>
              <div class="text-subtitle1">$50.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento6.jpeg" />
            <q-card-section>
              <div class="text-h6">nct dream character</div>
              <div class="text-subtitle1">$99.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento7.jpg" />
            <q-card-section>
              <div class="text-h6">animals character</div>
              <div class="text-subtitle1">$80.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento8.jpg" />
            <q-card-section>
              <div class="text-h6">cat character</div>
              <div class="text-subtitle1">$60.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento9.jpg" />
            <q-card-section>
              <div class="text-h6">giraffe character</div>
              <div class="text-subtitle1">$65.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento10.jpg" />
            <q-card-section>
              <div class="text-h6">doraemon character</div>
              <div class="text-subtitle1">$50.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento11.jpg" />
            <q-card-section>
              <div class="text-h6">keroppi character</div>
              <div class="text-subtitle1">$60.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

          <q-card class="my-card">
            <q-img src="./assets/bento12.jpg" />
            <q-card-section>
              <div class="text-h6">bear character</div>
              <div class="text-subtitle1">$55.000</div>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="order" color="primary" />
            </q-card-actions>
          </q-card>

        </div>

      </q-page>
    </q-page-container>

<!-- Membuat Footer -->
    <footer>
	      <p>&copy; copy right by cipa @nurasyifah_</p>
    </footer>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const slide = ref(1)
    const rightDrawerOpen = ref(false)
    const activeTab = ref('home')

    const toggleRightDrawer = () => {
      rightDrawerOpen.value = !rightDrawerOpen.value
    }

    const navigateTo = (tab) => {
      activeTab.value = tab
    }

    return {
      slide,
      rightDrawerOpen,
      toggleRightDrawer,
      activeTab,
      navigateTo
    }
  }
}
</script>

<style lang="scss" scoped>
.carousel-height {
  height: 400px; 
}

.my-card {
  width: 100%;
  max-width: 250px;
}
.container{
  background-color:#f6f5f2;
}

.paragraf1, .paragraf2 {
  width: 45%;
}

.paragraf1 {
  font-size: 25px;
  font-family: 'Informal Roman', sans-serif;
  text-align: justify;
  margin-left: 40px;
  padding-top: 70px;
  padding-bottom: 200px;
  color: black;
}

.paragraf2{
  font-size: 25px;
  font-family: 'Informal Roman', sans-serif;
  text-align: justify;
  position: absolute;
  margin-left: 620px;
  margin-top: -345px;
  color: black;
}

.q-tabs {
  margin-right: 500px;
}

footer {
  position: relative;
  width: 100%;
  height: 50px; 
  background: rgb(235, 230, 87);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 8px 0; 
  font-size: 13px;
  color: black;
}

footer, footer p {
  color: black !important; 
}
</style>
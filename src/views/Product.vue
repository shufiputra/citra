<template>
    <div class="ProductItem">
        <HeaderCitra />

        <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section text-left">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom"> 
                                <img class="product-big-img" :src="gambar_default" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel :dots="false" :nav="false" class="product-thumbs-track ps-slider">
                                    <div class="pt" @click="changeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : '' ">
                                        <img src="img/tilemustard1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[1])" :class="thumbs[1] == gambar_default ? 'active' : '' ">
                                        <img src="img/tilemustard2.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[2])" :class="thumbs[2] == gambar_default ? 'active' : '' ">
                                        <img src="img/tilemustard3.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[3])" :class="thumbs[3] == gambar_default ? 'active' : '' ">
                                        <img src="img/tilemustard4.jpg" alt="" />
                                    </div>

                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details text-left">
                                <div class="pd-title">
                                    <span>Flower</span>
                                    <h3>Tile Mustard</h3>
                                </div>
                                <div class="pd-desc">
                                    <br>
                                    <p>
                                        <h6>DESKRIPSI PRODUK</h6>
                                        <br>
                                        <h6>INFORMASI PRODUK</h6>
                                        <br>
                                        <h6>Ukuran: 115 x 115 cm</h6>
                                        <h6>Bahan: Voal Premium</h6>
                                        <h6>Finishing: Laser Cut</h6>
                                        <h6>Gold Charm / Plat Logo</h6>
                                        <br>
                                        Kesamaan warna dengan yang asli 98% (karena efek cahaya dan layar masing-masing perangkat) 
                                    </p>
                                    <br><br>
                                    <p>
                                        <h6>PRODUCT INFORMATION</h6>
                                        <br>
                                        <h6>Size : 115 x 115 cm</h6>
                                        <h6>Material : Premium Voile</h6>
                                        <h6>Finishing : Laser Cut</h6>
                                        <h6>With Gold Charm</h6>
                                        <br>
                                        Color similarity to the original is 98% (due to the light and screen effect of each handphone)
                                    </p>
                                    <h4>Rp. 200.000</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart"><a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a></router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

        <RelatedCitra />

        <FooterCitra />
    </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderCitra from "@/components/HeaderCitra.vue"
import FooterCitra from "@/components/FooterCitra.vue"
import RelatedCitra from "@/components/RelatedCitra.vue"

import carousel from "vue-owl-carousel";

export default {
    name: "ProductItem",
    components: {
        HeaderCitra,
        FooterCitra,
        RelatedCitra,
        carousel
    },
    data() {
        return {
            gambar_default: "img/tilemustard.jpg",
            thumbs: [
                "img/tilemustard1.jpg",
                "img/tilemustard2.jpg",
                "img/tilemustard3.jpg",
                "img/tilemustard4.jpg"
            ]
        }
    },

    methods: {
    changeImage(urlImage) {
        this.gambar_default = urlImage;
    }
    }
};

</script>

<style scoped>
.product-thumbs .pt {
    margin-right: 14px;
}

</style>
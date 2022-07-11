<template>
  <div class="HomeView">
    <HeaderCitra />
    <HeroCitra />
    <WomanCitra />
    <InstaCitra />
    <PartnerCitra />
    <FooterCitra />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderCitra from "@/components/HeaderCitra.vue"
import HeroCitra from "@/components/HeroCitra.vue"
import WomanCitra from "@/components/WomanCitra.vue"
import InstaCitra from "@/components/InstaCitra.vue"
import PartnerCitra from "@/components/PartnerCitra.vue"
import FooterCitra from "@/components/FooterCitra.vue"

export default {
  name: "HomeView",
  components: {
    HeaderCitra,
    HeroCitra,
    WomanCitra,
    InstaCitra,
    PartnerCitra,
    FooterCitra
  }
};
</script>

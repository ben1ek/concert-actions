<template>
  <v-footer app height="50">
    <div class="siteFooter d-flex align-center justify-space-between mx-auto px-4">
      <span>&#169; 2012 - 2025 Linkin Park - Poland</span>
      <div class="siteFooter_socials d-flex align-center">
        <v-icon :size="24" icon="mdi-youtube" @click="openYoutubeChannel"></v-icon>
        <v-icon :size="24" icon="mdi-instagram" @click="openInstagramPage"></v-icon>
        <v-icon :size="24" icon="mdi-facebook" @click="openFacebookPage"></v-icon>
      </div>
    </div>
  </v-footer>
</template>

<script lang="ts">
import { Component, Vue, toNative } from 'vue-facing-decorator';

@Component({
    name: 'SiteFooter'
})
class SiteFooter extends Vue {
  readonly FACEBOOK_URL = 'https://www.facebook.com/LPPoland';
  readonly YOUTUBE_URL = 'https://www.youtube.com/@LinkinParkPoland';
  readonly INSTAGRAM_URL = 'https://www.instagram.com/lppoland/';

  openFacebookPage(): void {
    window.open(this.FACEBOOK_URL, '_blank');
  }

  openYoutubeChannel(): void {
    window.open(this.YOUTUBE_URL, '_blank');
  }

  openInstagramPage(): void {
    window.open(this.INSTAGRAM_URL, '_blank');
  }
}

export default toNative(SiteFooter)
</script>

<style lang="scss">
  .siteFooter {
    user-select: none;
    max-width: 900px;
    width: 100%;
    &_socials {
      column-gap: 12px;
    }
    @media (max-width: 599px) {
      flex-direction: column;
      span {
        order: 2;
        font-size: 12px;
      }
    }
  }
</style>

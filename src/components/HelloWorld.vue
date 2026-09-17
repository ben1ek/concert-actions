<template>
  <v-container class="fill-height" max-width="900">
    <div class="mx-auto">
      <v-img class="siteLogo mb-4" height="150" @click="openFacebookPage" src="@/assets/logo.webp" />
      <div class="mb-8 text-center">
        <div class="text-body-2 font-weight-regular mb-n1">POLAND</div>
        <h1 class="text-h2 font-weight-bold">LINKIN PARK</h1>
      </div>
    </div>
    <div class="actionsContainer pa-4">
      <h2 class="font-weight-bold text-center mb-6">Open'er Festival 2025 - Akcje koncertowe</h2>
      <div class="action d-flex">
        <img src="@/assets/welcome-back.webp" alt="Welcome back" class="mr-4" />
        <div class="d-flex flex-column justify-space-around">
          <h3 class="mb-2">Kartki "Welcome back"</h3>
          <p class="mb-2">Na początku koncertu wszyscy podnosimy kartki z napisem "WELCOME BACK", tworząc niesamowity widok dla zespołu. Pokażmy im naszą jedność, wsparcie i wdzięczność za powrót! Link do pobrania kartki: <a target="_blank" href="https://bit.ly/welcome-back-lp">https://bit.ly/welcome-back-lp</a> 🖤</p>
          <v-btn append-icon="mdi-chevron-triple-right" :ripple="false" variant="outlined" @click="openAction1">Czytaj więcej</v-btn>
        </div>
      </div>
      <v-divider class="my-4"/>
      <div class="action d-flex">
        <img src="@/assets/one-more-light.webp" alt="Wspólne śpiewanie One More Light" class="mr-4" />
        <div class="d-flex flex-column justify-space-around">
          <h3 class="mb-2">Wspólne śpiewanie "One More Light"</h3>
          <p class="mb-2">Podczas przerwy przed bisem (zaraz po utworze "One Step Closer") chcemy razem, jako jedna społeczność, zaśpiewać pierwszą zwrotkę i refren "One More Light" dla Chestera Benningtona. To będzie nasz muzyczny hołd, nasz gest pamięci i miłości. ❤️</p>
          <v-btn append-icon="mdi-chevron-triple-right" :ripple="false" variant="outlined" @click="openAction2">Czytaj więcej</v-btn>
        </div>
      </div>
      <v-divider class="my-4"/>
      <div class="action d-flex">
        <img src="@/assets/morze-swiatel.webp" alt="Morze świateł" class="mr-4" />
        <div class="d-flex flex-column justify-space-around">
          <h3 class="mb-2">Morze świateł na utworze "Lost"</h3>
          <p class="mb-2">Podczas fortepianowego intra do utworu "Lost", wszyscy włączamy latarki w telefonach i unosimy je w górę. Chcemy stworzyć niezapomniany widok tysięcy świateł, który poruszy serca nie tylko zespołu, ale i całej publiczności! ✨</p>
          <v-btn append-icon="mdi-chevron-triple-right" :ripple="false" variant="outlined" @click="openAction3">Czytaj więcej</v-btn>
        </div>
      </div>
      <v-divider class="my-4"/>
      <div class="action d-flex">
        <img src="@/assets/this-is-what-we-asked-for.webp" alt="This is what we asked for" class="mr-4" />
        <div class="d-flex flex-column justify-space-around">
          <h3 class="mb-2">Flaga sektorowa</h3>
          <p class="mb-2">Przygotowujemy <a target="_blank" href="https://youtu.be/DbksdPQwZj4?si=3OcRIeXLXw4W6gnS">flagę sektorową</a> "This is what we asked for", którą chcemy zaprezentować zespołowi podczas koncertu. Będzie to najlepszy możliwy sposób na pokazanie mu, że doceniamy to, że powrócił do występowania i że dziękujemy za przyjazd do naszego kraju. 🏳️</p>
          <v-btn append-icon="mdi-chevron-triple-right" :ripple="false" variant="outlined" @click="openAction4">Czytaj więcej</v-btn>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script setup lang="ts">
const ACTION_1 = 'https://www.facebook.com/LPPoland/posts/pfbid0zNfQ6ZrVDFAZ8xnr2VNVtoEveCdfi2F63UK641EK7gjUo7pmhbpHbQzmFQydvGRYl';

const ACTION_2 = 'https://www.facebook.com/LPPoland/posts/pfbid0daSQm3N8jGadVWikmhXgzrPcPcqLShq2Vytiybbed9HbYBX7VsVEKP1fU3m7Zxaql';

const ACTION_3 = 'https://www.facebook.com/LPPoland/posts/pfbid02byihbTccdYa4ZpiuiD6EBxKPXkkGLzerMKCPgqWPBcnad8UUnsUUyJygHPF1iGrxl';

const ACTION_4 = 'https://www.facebook.com/LPPoland/posts/pfbid02yWKsbZNdx81ZVMKgdT6ayAWxd592stCXF8vxv37xsdBM8yTeSbLdPsXusanzNLT8l';

function openAction1(): void {
  window.open(ACTION_1, '_blank');
}

function openAction2(): void {
  window.open(ACTION_2, '_blank');
}

function openAction3(): void {
  window.open(ACTION_3, '_blank');
}

function openAction4(): void {
  window.open(ACTION_4, '_blank');
}

function openFacebookPage(): void {
  window.open('https://www.facebook.com/LPPoland', '_blank');
}
</script>
<style lang="scss">
.v-container {
  user-select: none;
}
.siteLogo {
  cursor: pointer;
}
.actionsContainer {
  user-select: none;
  background-color: #282828;
  width: 100%;
  border-radius: 8px;
  h2 {
    font-size: 24px;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 13px;
  }
  button {
    width: fit-content;
    .v-btn__append i {
      margin-top: -1px;
    }
  }
  .action {
    img {
      width: 213px;
      height: 150px;
      object-fit: cover;
      border-radius: 8px;
    }
  }
  @media (max-width: 599px) {
    .action {
      flex-direction: column;
      align-items: center;
      img {
        margin-right: 0 !important;
        margin-bottom: 8px;
      }
      h3, p {
        text-align: center;
      }
      button {
        margin: 0 auto;
      }
    }
  }
}
@media (max-width: 599px) {
  h1.text-h2 {
    font-size: 2.5rem !important;
  }
}
</style>

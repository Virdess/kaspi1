<template>
  <ion-app>
    <ion-header style="background: none;">
      <div style="margin-bottom: 10px; margin-top: 10px;">
        <ion-buttons slot="start">
          <ion-back-button><img src="./back.png" alt="" height="30px"></ion-back-button>
        </ion-buttons>
        <ion-title style="font-size: 16px;">Удостоверение личности</ion-title>
      </div>
    </ion-header>

    <ion-content style="height: calc(100vh - var(--ion-safe-area-top) - var(--ion-safe-area-bottom));">
      <ion-segment style="width: 90%; margin: 0 auto;">
        <ion-segment-button value="document" checked>
          <ion-label>Документ</ion-label>
        </ion-segment-button>
        <ion-segment-button value="details">
          <ion-label>Реквизиты</ion-label>
        </ion-segment-button>
      </ion-segment>

      <div style="text-align: center; margin-top: 20px;">
        <!-- Используем <img> для реального изображения -->
        <img src="./Screenshot_2023-03-08-08-07-24-390_kz.kaspi.mobile.png" alt="">
      </div>
    </ion-content>

    <ion-footer style="position: absolute; bottom: 0; width: 100%; --ion-safe-area-bottom: env(safe-area-inset-bottom);">
      <ion-grid>
        <ion-row>
          <ion-col size="12">
            <ion-button expand="block"><img src="./qr.png" alt="" height="80%"> Предъявить документ</ion-button>
          </ion-col>
          <ion-col size="12">
            <ion-button expand="block" color="primary" fill="outline"><img src="./exp.png" alt="" height="80%"> Отправить документ</ion-button>
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-footer>
  </ion-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  name: 'App',
  mounted() {
  }
});
</script>

<style scoped>
.image-container {
  text-align: center;
  margin-top: 20px;
}

ion-footer {
  padding: 20px 0;
}

ion-button {
  margin: 10px 0;
  --background: #0175ca;
  --background-hover: #006dbb;
  --background-activated: #006dbb;
  --background-focused: #006dbb;
}

.toolbar-background {
  background: white;
  border: none;
}

:host {
  --background: white;
}

@media (min-width: 600px) {
  ion-content {
    height: calc(100vh - var(--ion-safe-area-top) - var(--ion-safe-area-bottom));
  }
}

@media (max-width: 599px) {
  ion-content {
    height: calc(100vh - var(--ion-safe-area-top) - var(--ion-safe-area-bottom));
  }
}
</style>

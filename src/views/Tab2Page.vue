<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-fab vertical="bottom" horizontal="center" slot="fixed">
        <ion-fab-button @click="takePhoto()">
          <ion-icon :icon="Icons['camera']"></ion-icon>
        </ion-fab-button>
      </ion-fab>
      <ion-grid>
        <ion-row>
          <ion-col size="6" :key="photo" v-for="photo in photos">
            <ion-img :src="photo.webviewPath"></ion-img>
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import {
  IonPage,
  IonFab,
  IonFabButton,
  IonGrid,
  IonRow,
  IonImg,
  IonCol,
  IonContent,
  IonIcon,
} from "@ionic/vue";
import * as Icons from "ionicons/icons";
import { usePhotoGallery, UserPhoto } from "@/composables/usePhotoGallery";

export default defineComponent({
  name: "Tab2Page",
  components: {
    IonContent,
    IonPage,
    IonFab,
    IonFabButton,
    IonIcon,
    IonGrid,
    IonImg,
    IonRow,
    IonCol,
  },
  data() {
    return { Icons };
  },
  setup() {
    const { photos, takePhoto } = usePhotoGallery();

    return {
      photos,
      takePhoto,
    };
  },
});
</script>
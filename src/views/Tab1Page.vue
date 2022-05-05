<template>
  <ion-page>
    <ion-content :fullscreen="true" class="background-image">
      <ion-card class="h-card">
        <ion-card-header>
          <ion-card-title>Title</ion-card-title>
          <ion-card-subtitle>Secondary text 2</ion-card-subtitle>
        </ion-card-header>
        <span class="delay">
          <ion-icon :icon="Icons['timer']"></ion-icon>
          Il vous reste 14h
        </span>
      </ion-card>
      <div class="ion-padding-start horizontal-scroll">
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
        <ion-chip>
          <ion-label>Default</ion-label>
        </ion-chip>
      </div>
      <ion-row class="ion-padding">
        <ion-col>
          <ion-card>
            <img src="https://picsum.photos/200" />
            <ion-card-header class="ion-padding-top no-p-b">
              <ion-card-subtitle>overline</ion-card-subtitle>
              <ion-card-title>Title</ion-card-title>
            </ion-card-header>
            <span class="delay">
              <ion-icon :icon="Icons['timer']"></ion-icon>
              1J
            </span>
            <ion-card-content> Secondary text 2 </ion-card-content>
          </ion-card>
        </ion-col>
        <ion-col>
          <ion-card>
            <img src="../../public/assets/img.jpeg" />
            <ion-card-header class="ion-padding-top no-p-b">
              <ion-card-subtitle>overline</ion-card-subtitle>
              <ion-card-title>Title</ion-card-title>
            </ion-card-header>
            <span class="delay">
              <ion-icon :icon="Icons['timer']"></ion-icon>
              1J
            </span>
            <ion-card-content> Secondary text 2 </ion-card-content>
          </ion-card>
        </ion-col>
        <ion-col>
          <ion-card>
            <img src="https://picsum.photos/200" />
            <ion-card-header class="ion-padding-top no-p-b">
              <ion-card-subtitle>overline</ion-card-subtitle>
              <ion-card-title>Title</ion-card-title>
            </ion-card-header>
            <span class="delay">
              <ion-icon :icon="Icons['timer']"></ion-icon>
              1J
            </span>
            <ion-card-content> Secondary text 2 </ion-card-content>
          </ion-card>
        </ion-col>
        <ion-col>
          <ion-card>
            <img src="https://picsum.photos/200" />
            <ion-card-header class="ion-padding-top no-p-b">
              <ion-card-subtitle>overline</ion-card-subtitle>
              <ion-card-title>Title</ion-card-title>
            </ion-card-header>
            <span class="delay">
              <ion-icon :icon="Icons['timer']"></ion-icon>
              1J
            </span>
            <ion-card-content>
              Secondary text 2
            </ion-card-content>
          </ion-card>
        </ion-col>
      </ion-row>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import {
  IonPage,
  IonCard,
  IonCardHeader,
  IonCardTitle,
  IonCardSubtitle,
  IonCardContent,
  IonRow,
  IonCol,
  IonContent,
  IonIcon,
  IonChip,
  IonLabel,
} from "@ionic/vue";
import * as Icons from "ionicons/icons";

export default defineComponent({
  name: "Tab1Page",
  components: {
    IonContent,
    IonPage,
    IonIcon,
    IonCard,
    IonCardContent,
    IonRow,
    IonCol,
    IonChip,
    IonLabel,
    IonCardHeader,
    IonCardTitle,
    IonCardSubtitle,
  },
  data() {
    return { Icons };
  },
});
</script>
<style scoped>
.h-card {
  margin-top: 50px;
  border-radius: 30px;
  background-color: #c4c4c4;
  box-shadow: none;
  min-height: 150px;
}
.delay {
  position: absolute;
  top: 10px;
  right: 10px;
  background: white;
  border-radius: 15px;
  padding: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 5px;
}
.delay ion-icon {
  font-size: 20px;
}
.horizontal-scroll {
  overflow: auto;
  white-space: nowrap;
}
.no-p-b {
  padding-bottom: 0px;
}
ion-row.ion-padding {
  gap: 20px;
  margin-bottom: 30px;
}
ion-row ion-card {
  border-radius: 25px;
  margin: 0;
}
ion-row ion-card ion-card-subtitle {
  font-size: 10px;
}
ion-row ion-card ion-card-title {
  font-weight: normal;
  font-size: 16px;
}
ion-col:nth-child(2n) {
  top: 50px;
}
.background-image {
  --background: url(../../public/background.png) 0 0/100% 100% no-repeat;
}

::-webkit-scrollbar,
*::-webkit-scrollbar {
  display: none;
  overflow: hidden;
}
</style>
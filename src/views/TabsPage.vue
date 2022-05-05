<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="tab1" href="/tabs/tab1">
          <ion-icon :icon="Icons['albums']"></ion-icon>
        </ion-tab-button>

        <ion-tab-button tab="tab2" href="/tabs/tab2">
          <ion-icon :icon="Icons['add']"></ion-icon>
        </ion-tab-button>

        <ion-tab-button tab="tab3" href="/tabs/tab3">
          <ion-icon :icon="Icons['person']"></ion-icon>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import {
  IonTabBar,
  IonTabButton,
  IonTabs,
  IonIcon,
  IonPage,
  IonRouterOutlet,
} from "@ionic/vue";
import * as Icons from "ionicons/icons";

export default defineComponent({
  name: "TabsPage",
  components: {
    IonTabs,
    IonTabBar,
    IonTabButton,
    IonIcon,
    IonPage,
    IonRouterOutlet,
  },
  data() {
    return { Icons };
  },
});
</script>
<style scoped>
ion-tab-bar {
  background-color: black;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  border: unset;
}

ion-tab-button {
  background-color: black;
}

ion-tabs {
  background: url(../../public/background.png) 0 0/100% 100% no-repeat;
}

ion-tab-button {
  --color-selected: var(--ion-color-light);
}
</style>
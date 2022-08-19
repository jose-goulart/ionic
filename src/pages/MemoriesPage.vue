<template>
  <base-layout page-title="All Memories">
    <ion-list>
      <ion-item router-link="/memories/1">A trip into the montains</ion-item>
      <ion-item>Surfing the sea side</ion-item>
      <ion-item>Good eating</ion-item>
    </ion-list>
  </base-layout>
</template>

<script>

import { 
  IonList,
  IonItem
} from '@ionic/vue';

export default {
  components: {
    IonList,
    IonItem
  },
  data() {
    return {
      memories: [
        { 
        id: 'm1', 
        image: 'https://www.atlasandboots.com/wp-content/uploads/2019/05/ama-dablam2-most-beautiful-mountains-in-the-world.jpg',
        title: 'A trip into the montains', 
        description: 'It was a really nice trip!' 
        },
        { 
        id: 'm2', 
        image: 'https://www.lifegate.com/app/uploads/mare-fa-bene-2.jpg',
        title: 'Surfing the sea side', 
        description: 'Feeling the cool breeze.' 
        },
        { 
        id: 'm3', 
        image: 'https://upload.wikimedia.org/wikipedia/commons/6/6d/Good_Food_Display_-_NCI_Visuals_Online.jpg',
        title: 'Good eating', 
        description: 'Really tasty!' 
        },
      ]
    }
  }
}
</script>
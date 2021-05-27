<template>
  <q-page class="constrain q-pa-md">
    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card
          class="card-post q-mb-md"
          v-for="post in posts"
          :key="post.id"
          flat
          bordered
        >
          <q-item>
            <q-item-section avatar>
              <q-avatar size="48px">
                <img
                  src="https://pbs.twimg.com/profile_images/1042481460144431104/AgPl0tuH_400x400.jpg"
                />
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">erbek_h</q-item-label>
              <q-item-label caption>{{ post.location }} </q-item-label>
            </q-item-section>
          </q-item>
          <q-separator />
          <q-img :src="post.imageURL" />
          <q-card-section>
            <div>{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ post.date | niceDate }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://pbs.twimg.com/profile_images/1042481460144431104/AgPl0tuH_400x400.jpg"
              />
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label class="text-bold">erbek_h</q-item-label>
            <q-item-label caption>Hüseyin ERBEK</q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
import {date} from 'quasar'
export default {
  name: 'PageHome',
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: 'Golden Gate',
          date: 1622142452715,
          location: 'San Farncisco',
          imageURL: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 2,
          caption: 'Cami ve Köprü İstanbul',
          date: 1622142452715,
          location: 'İstanbul',
          imageURL: 'https://www.hisglobal.com.tr/assets/images/1581429467.jpg'
        },
        {
          id: 3,
          caption: 'Ankara Manzarası',
          date: 1622142452715,
          location: 'Ankara',
          imageURL:
            'https://image.arrivalguides.com/415x300/09/aaafe2acddd3f57b18e34f8382d9721b.jpg'
        },
        {
          id: 4,
          caption: 'Hasta la victoria siempre ',
          date: 1622142452715,
          location: 'Ankara',
          imageURL:
            'https://cdntr1.img.sputniknews.com/img/101423/35/1014233574_0:66:1024:620_1000x541_80_0_0_46307f69bc2947e460598e2b780267a6.jpg'
        }
      ]
    }
  },
  filters: {
    niceDate(value) {
      return date.formatDate(value, 'MMM D h:mmA')
    }
  }
}
</script>
<style lang="sass">
.car_post
  .q-img
    min-height: 200px
</style>

<template>
  <q-layout view="hhh lpR fFf">
    <q-header elevated class="bg-negative">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          TESTE
        </q-toolbar-title>

        <div>Quasar v</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      overlay
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Dashboard
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Exemplo 1',
    icon: 'school'
  },
  {
    title: 'Exemplo 2',
    icon: 'code'
  },
  {
    title: 'Exemplo 3',
    icon: 'chat'
  },
  {
    title: 'Exemplo 4',
    icon: 'record_voice_over'
  },
  {
    title: 'Exemplo 5',
    icon: 'rss_feed'
  }
]

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

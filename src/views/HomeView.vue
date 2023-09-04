<template>
  <v-container>
    <HelloWorld/>
  </v-container>
</template>

<script>

export default
{
  name: 'HomeView',

  components: {
    HelloWorld: () => import('@/components/HelloWorld.vue'),
  },
};
</script>

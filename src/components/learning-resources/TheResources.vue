<template>
  <base-card>
    <base-button @click="setSelectedTab('stored-resources')"
      >Stored Resources</base-button
    >
    <base-button @click="setSelectedTab('add-resources')"
      >Add Resources</base-button
    >
  </base-card>
  <component :is="selectedTab"> </component>
</template>

<script>
import BaseButton from '../../UI/BaseButton.vue';
import BaseCard from '../../UI/BaseCard.vue';
import StoredResources from './StoredResources.vue';
import AddResources from './AddResources.vue';

export default {
  components: {
    BaseCardBaseButton,
    StoredResources,
    AddResources,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>

<style scoped></style>

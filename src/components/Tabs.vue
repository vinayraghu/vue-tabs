<template>
  <article class="grid">
    <section class="tab-titles">
      <div class="chewy-tab-title" @click="setActive('apple')">Apple</div>
      <div class="chewy-tab-title" @click="setActive('banana')">Banana</div>
      <div class="chewy-tab-title" @click="setActive('cherry')">Cherry</div>
    </section>
    <section>
      <div
        class="chewy-tab-panel"
        :class="activeTab === 'apple' && 'chewy-tab-panel--active'"
      >
        Apples are good
      </div>
      <div
        class="chewy-tab-panel"
        :class="activeTab === 'banana' && 'chewy-tab-panel--active'"
      >
        Bananas are great
      </div>
      <div
        class="chewy-tab-panel"
        :class="activeTab === 'cherry' && 'chewy-tab-panel--active'"
      >
        Cherries are fantastic
      </div>
    </section>
  </article>
</template>
<script>
export default {
  name: "Tabs",
  data() {
    return {
      activeTab: "apple",
    };
  },
  methods: {
    setActive(str) {
      this.activeTab = str;
    },
  },
};
</script>
<style lang="scss">
@import "./chewy-tabs.css";
.tab-titles {
  // display: flex;
}
.grid {
  display: grid;
  grid-template-columns: 30% 70%;
}
</style>

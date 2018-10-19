<template>
  <div class="level-2"> 
    <a class="heading collapsed" data-toggle="collapse" :href="'#campaign-'+uid" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h3>{{ title }}</h3>
    </a>
    <div class="collapse mb-2" :id="'campaign-'+uid">
      <div v-for="(item, index) in link" :key="index" class="d-flex flex-column email-links align-items-start">
        <p class="bold">{{ item.heading }}</p>
        <p>{{ item.subheading }}</p>
        <a :href="item.url" target="_blank">{{ item.link }}</a>
      </div>
    </div>
  </div> 
</template>

<script>
let uid = 1;

export default {
  name: 'Campaign',
  props: {
    title: String,
    link: Array
  },
  beforeCreate() {
    this.uid = uid.toString();
    uid += 1;
  },
};
</script>
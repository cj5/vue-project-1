<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+category" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>{{ category }}</h2>
    </a>
    <div class="collapse" :id="category">
      <Campaign 
        :id="category+'-campaign-1'"
        title=""
        :link="[
          { heading: '', subheading: '', link: '', url: '#' },
        ]"
      />
    </div>
  </div>
</template>

<script>
import Campaign from './Campaign';

export default {
  data: () => {
    return {
      category: ''
    }
  },
  components: { Campaign },
};
</script>
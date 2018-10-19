<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+category" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>{{ category }}</h2>
    </a>
    <div class="collapse" :id="category">
      <Campaign
        title="2019 Moments Site"
        :link="[
          { heading: 'Reminder | 04.18.18', link: 'View Email 1', url: 'http://chrisstack.co' },
          { link: 'View Email 2', url: 'http://chrisstack.co' },
        ]"
      />
      <Campaign
        title="Annual choice benefit - choice of email"
        :link="[
          { heading: 'Reminder | 04.18.18', link: 'View Email 1', url: 'http://chrisstack.co' },
          { link: 'View Email 2', url: 'http://chrisstack.co' },
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
      category: 'ongoing'
    }
  },
  components: { Campaign }
};
</script>
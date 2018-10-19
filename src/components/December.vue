<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+category" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>{{ category }}</h2>
    </a>
    <div class="collapse" :id="category">
      <Campaign
        title="Campaign 1"
        :link="[
          { heading: 'Heading test', subheading: 'Subheading', link: 'View Email 1', url: 'http://chrisstack.co' },
          { heading: 'TEST', link: 'View Email 2', url: 'http://reddit.com' },
          { link: 'View Email 3', url: 'http://reddit.com' },
        ]"
      />
      <Campaign
        title="Campaign 2"
        :link="[
          { heading: 'Testeroni', link: 'View Email 1', url: 'http://chrisstack.co' },
          { link: 'View Email 2', url: 'http://reddit.com' },
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
      category: 'december'
    }
  },
  components: { Campaign },
};
</script>
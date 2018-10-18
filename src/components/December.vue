<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" href="#december" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>december</h2>
    </a>
    <div class="collapse" id="december">
      <Campaign
        id="december-campaign-1"
        title="Campaign 1"
        subheading="Sub-heading 1"
        :link="[
          { link: 'View Email 1', url: 'http://chrisstack.co' },
          { link: 'View Email 2', url: 'http://reddit.com' },
          { link: 'View Email 3', url: 'http://reddit.com' },
        ]"
      />
      <Campaign
        id="december-campaign-2"
        title="Campaign 2"
        subheading="Sub-heading 2"
        :link="[
          { link: 'View Email 1', url: 'http://chrisstack.co' },
          { link: 'View Email 2', url: 'http://reddit.com' },
        ]"
      />
    </div>
  </div>  
</template>

<script>
import Campaign from './Campaign.vue';

export default {
  name: 'December',
  components: { Campaign }
};
</script>
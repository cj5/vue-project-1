<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" href="#ongoing" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>Ongoing</h2>
    </a>
    <div class="collapse" id="ongoing">
      <Campaign
        id="ongoing-campaign-1"
        title="2019 Moments Site"
        subheading=""
        :link="[
          { link: 'View Email 1', url: 'http://chrisstack.co'},
          { link: 'View Email 2', url: 'http://chrisstack.co'},
        ]"
      />
      <Campaign
        id="ongoing-campaign-2"
        title="Annual choice benefit - choice of email"
        subheading="Reminder | 04.18.18"
        :link="[
          { link: 'View Email 1', url: 'http://chrisstack.co'},
          { link: 'View Email 2', url: 'http://chrisstack.co'},
        ]"
      />
    </div>
  </div>  
</template>

<script>
import Campaign from './Campaign.vue';

export default {
  name: 'Ongoing',
  props: ['title'],
  components: { Campaign }
};
</script>
<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+category" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>{{ category }}</h2>
    </a>
    <div class="collapse" :id="category">
      <Campaign 
        title="CA Q4 Acq &amp; MGM"
        :link="[
          { heading: 'Round 01 | 09.10.17', subheading: 'ACQ Emails:' },
          { link: 'Balance', url: '#' },
          { link: 'Elite', url: '#' },
          { link: 'General', url: '#' },
          { link: 'New', url: '#' },
          { subheading: 'MGM Emails:' },
          { link: 'Business', url: '#' },
          { link: 'Consumer', url: '#' },
        ]"
      />
      <Campaign
        title="Fifth Year SPG/AMEX Happy Hour Promotion"
        :link="[
          { heading: 'Round 01 | 10.05.18' },
          { link: 'View Email', url: '#' }
        ]"
      />
      <Campaign
        title="US Amex Lux Card Event Invite"
        :link="[
          { link: 'View Email', url: '#' }
        ]"
      />
      <Campaign
        title="US Amex Small Biz Campaign"
        :link="[
          { link: 'View Email', url: '#' }
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
      category: 'october'
    }
  },
  components: { Campaign },  
};
</script>
<template>
  <div class="level-1">
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+category" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h2>{{ category }}</h2>
    </a>
    <div class="collapse" :id="category">
      <Campaign
        title="US Amex Q3 MGM"
        :link="[
          { heading: 'Wave 2 | 08.30.2018', subheading: 'MGM:', link: 'Business', url: '#' },
          { link: 'Consumer', url: '#' },
          { link: 'Luxury', url: '#' },
          { subheading: 'ACQ:', link: 'View Email', url: '#' },
          { heading: 'Round 2 | 08.30.2018', subheading: 'MGM:', link: 'Business', url: '#' },
          { link: 'Consumer', url: '#' },
          { link: 'Luxury', url: '#' },
          { subheading: 'ACQ:', link: 'View Email', url: '#' },
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
      category: 'november'
    }
  },
  components: { Campaign },
};
</script>
<template>
  <div class="level-2"> 
    <a class="heading collapsed" data-toggle="collapse" :href="'#'+id" role="button" aria-expanded="false" aria-controls="collapseExample">
      <h3>{{ title }}</h3>
    </a>
    <div class="collapse" :id="id">
      <div class="d-flex flex-column email-links align-items-start">
        <p>{{ subheading }}</p>
        <ul>                  
          <li v-for="item in link"><a :href="item.url" target="_blank">{{ item.link }}</a></li>
        </ul>
      </div>
    </div>
  </div> 
</template>

<script>
export default {
  name: 'Campaign',
  props: {
    id: String,
    title: String,
    subheading: String,
    link: Array
  },
};
</script>
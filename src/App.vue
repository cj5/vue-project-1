<template>
  <div id="app">
    <div class="wrapper">
      <div class="header d-flex justify-content-between align-items-end">
        <h1 class="uppercase red">Client Review</h1>
        <div class="logo"></div>
      </div>
    
      <div class="accordion">
        <Ongoing />
        <December />
      </div>
    </div>
  </div>
</template>

<script>
import Ongoing from "./components/Ongoing";
import December from "./components/December";

export default {
  name: "App",
  components: {
    Ongoing,
    December
  }
};
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* GENERAL STYLES */
.uppercase {
  text-transform: uppercase;
}
.red {
  color: #cf152d;
}
.wrapper a {
  text-decoration: none;
}
.wrapper a:hover {
  text-decoration: none;
}
h1,
h2,
h3,
h4,
h5 {
  margin: 0;
  text-transform: capitalize;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
/* END GENERAL STYLES */

body {
  background: url(images/bg_repeat.jpg) 0 0;
  overflow-y: scroll;
}
h1 {
  font-size: 32px;
  line-height: 36px;
}
h2 {
  font-size: 22px;
  line-height: 24px;
}
h3 {
  font-size: 16px;
  line-height: 18px;
}
.wrapper {
  max-width: 803px;
  background-color: #fff;
  padding: 0 21px 28px;
  margin: 0 auto 80px;
  min-width: 280px;
  position: relative;
  -webkit-box-shadow: 2px 2px 3px 3px rgba(216, 216, 216, 0.8);
  box-shadow: 2px 2px 3px 3px rgba(216, 216, 216, 0.8);
}
.header {
  padding: 50px 0;
}
.logo {
  background: url(images/tlgLogo.gif) no-repeat 0 0;
  background-size: cover;
  width: 164px;
  height: 114px;
}
.accordion {
  border: 1px solid #aaa;
}
.heading {
  position: relative;
}
.level-1 .heading {
  display: block;
  padding: 10px 20px;
  padding-left: 32px;
  background-color: #eee;
  color: #333;
  margin: 5px;
}
.heading *::before {
  content: "-";
  position: absolute;
  left: 10px;
  transform: translateY(-2px);
  /*color: #cf152d;*/
}
.heading.collapsed *::before {
  content: "+";
}
#february-category .heading.collapsed *::before {
  content: "";
}
#february-category a {
  cursor: default;
  color: #999;
}
.heading h3::before {
  left: 30px;
}
.level-1 .heading:hover {
  color: #333;
}
.level-2 .heading {
  background-color: #fff;
  padding: 4px 20px 4px 50px;
  font-size: 26px;
  color: #777;
  border: none !important;
  margin: 0;
}
.level-2 .heading:hover {
  color: #777;
}
.email-links {
  padding-left: 60px;
}
.email-links ul {
  margin-bottom: 10px;
}
.email-links li {
  line-height: 20px;
}
.email-links li p {
  font-weight: normal;
}
.email-links a {
  margin-left: 12px;
  font-size: 14px;
  color: #cf152d;
  transition: all 0.2s ease-in-out;
  border-bottom: 1px solid transparent;
}
.email-links a:hover {
  /*color: #000;*/
  border-bottom: 1px solid #cf152d;
}
/*.email-links a::after {
  content: ">";
  left: 5px;
  position: relative;
  transition: all 0.2s ease-in-out;
}*/
.email-links a:hover::after {
  /*left: 10px;*/
  /*color: #000;*/
}
.email-links p {
  font-size: 14px;
  font-weight: bold;
  margin: 0;
}

</style>

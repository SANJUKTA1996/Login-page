<template>
  <router-view />
</template>


<script>
export default {
  name: "App",
};
</script>


<style>
.form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  /* background-color: #ffa500; */
  /* background-color: #3c1a3991; */
      background-color: #6fa2cd;
  border-radius: 12px;
  padding: 20px;
}
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px;
  margin-top: 10px;
}
body {
  padding: 0;
  margin: 0;

  /* background-color: #87ceeb; */
 background-image: url("https://thumbs.dreamstime.com/b/white-snow-pattern-light-blue-background-patern-texture-winter-theme-35030570.jpg");
 opacity: 0.9;
 z-index: 99;
}
.register input,
.login input {
  background: #fff8dc;
  color: black;
  width: 200px;
  height: 30px;
  padding-left: 20px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  border-width: 1px;
  /* padding: 6px 15px 6px 35px; */
  padding: 1px 9px 0px 35px;
  border-radius: 12px;
  /* box-shadow: 0 0 4px 2px skyblue; */
  box-shadow: 0 0 0px 1px skyblue;
  transition: 500ms all ease;
  outline: 0;
  margin-bottom: 12px;
}

.textbox:hover {
  width: 260px;
}
.button {
  font-size: 12px;
  border-radius: 5px;
  border: solid 1px #3866a3;
  color: #fff;
  padding: 10px 18px;
  background: linear-gradient(180deg, #63b8ee 5%, #468ccf 100%);
  text-shadow: 1px 1px 0px #7cabde;
  box-shadow: inset 1px 1px 2px 0px #bee3f9;
  font-family: Arial;
  cursor: pointer;
  text-align: center;
  height: 35px;
  font-size: 15px;
  width: 100px;
  user-select: none;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  margin-top: 10px;
  text-align: center;
}
.text {
  font-size: 25px;

  font-family: "Roboto";
}
.css-button-2:hover {
  background: linear-gradient(180deg, #468ccf 5%, #63b8ee 100%);
}
.css-button-2:active {
  position: relative;
  top: 1px;
}
.btn-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.link-style{
  text-decoration: none;
}
.link-style:hover{
  text-decoration: underline;
}
</style>
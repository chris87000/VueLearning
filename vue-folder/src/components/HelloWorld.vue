<template>
  <div class="hello">
    <h2 :class="myH2">Hello</h2>
    <h1>{{ msg }}</h1>
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <h1>{{ gender }}</h1>
    <h1>{{ "Hello" }}</h1>
    </div>
    <button v-on:click="handleClick">Click</button>&nbsp;&nbsp;
    <button v-on:click="handleClick2(100)">Click2</button>&nbsp;&nbsp;
    <button v-on:click="onBtnClick( number )">Inc</button>
    <h2>{{ number }}</h2>
    <br/><br/>
    <h1 id="header">Header</h1>
    <div v-bind:id="myId">Hello my div: {{ myId }}</div>
    <img v-bind:src="mySrc" alt="" width="50%" height="50%"/>
    <div>
      <form @submit="handleSubmit">
       <label for="idInput">Input: <input type = "text" id="idInput" /></label>  <br/>
        <button type = "submit">Submit</button>
    </form>
    </div>
</template>

<script>
/* eslint-disable */ 
export default {
  name: 'HelloWorld',
  methods: {
    handleClick(event) {
      event.target.style.backgroundColor = 'red';
     // const header = document.getElementById('header');
     // header.style.color = 'red';
    },
    handleClick2(param) {
      console.log("PARAM", param);
    },
    onBtnClick(event, number) {
      this.number = this.number + 1;
      console.log("number", number);
    },
    handleSubmit(event) {
      event.preventDefault();
      console.log("Form Submit", document.getElementById('idInput').value);
    },
  },
  data() {
    return {
      name: 'John',
      age: 25,
      number: 1,
      gender: true,
      myId: 'divId',
      mySrc: 'https://www.turunculevye.com/wp-content/uploads/2025/03/Yeni-Assassins-Creed-Shadows-Videosu-Iki-Farkli-Gidisati-Gosteriyor.jpg',
      myH2: 'myH2',
    };
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#divId{
  background-color: red;
}
.myH2{
  background-color: red;
}
</style>

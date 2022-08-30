<script setup>
// exercise - intro to vue
let user = "Laura"

//exercise - rock paper scissor
let choices = ["rock", "paper", "scissors"]
let player1 = choices[Math.floor(Math.random() * 2)]
let player2 = prompt("rock, paper, or scissors?");

// Exercise - product listing
fetch('https://fakestoreapi.com/products')
    .then(data => data.json())
    .then(data => {
      let products = data
      console.log(products)
    })

</script>

<template>

<!--  exercise - intro to vue -->
  <h1>Hello {{ user }} {{ player1 }}!</h1>

<!--  exercise - rock paper scissors -->
<!--  <h2>Rock, Paper, Scissors</h2>-->
<!--  <h3>Player1 got: {{player1}} and Player2 got: {{player2}}</h3>-->
<!--<p v-if="player1 === player2">It's a tie! Play again</p>-->
<!--<p v-else-if="player1 === 'rock' && player2 === 'scissors'">Player 1-->
<!--  wins!</p>-->
<!--<p v-else-if="player1 === 'paper' && player2 === 'rock'">Player 1-->
<!--    wins!</p>-->
<!--<p v-else-if="player1 === 'scissors' && player2 === 'paper'">Player 1-->
<!--    wins!</p>-->
<!--<p v-else-if="player2 === 'rock' && player1 === 'scissors'">Player 2-->
<!--  wins!</p>-->
<!--<p v-else-if="player2 === 'paper' && player1 === 'rock'">Player 2-->
<!--  wins!</p>-->
<!--<p v-else-if="player2 === 'scissors' && player1 === 'paper'">Player 2-->
<!--  wins!</p>-->

<!-- exercise - product listing -->
  <h2>Product Listings</h2>
  <h2 v-for="product in {products}"></h2>
  <ul>
      <li v-for="product in products">
        {{product}}
        {{product.title}}
        {{product.description}}
        {{product.image}}
        <button>Add to Cart</button>
      </li>
  </ul>

</template>


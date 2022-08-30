<template>

<h1>Hello {{ user, player1, player2 }} !</h1>

  <h2>Rock, Paper, Scissors</h2>
  <h3>Player1 got: {{player1}} and Player2 got: {{player2}}</h3>
<p v-if="player1 === player2">It's a tie! Play again</p>
<p v-else-if="player1 === 'rock' && player2 === 'scissors'">Player 1
  wins!</p>
<p v-else-if="player1 === 'paper' && player2 === 'rock'">Player 1
    wins!</p>
<p v-else-if="player1 === 'scissors' && player2 === 'paper'">Player 1
    wins!</p>
<p v-else-if="player2 === 'rock' && player1 === 'scissors'">Player 2
  wins!</p>
<p v-else-if="player2 === 'paper' && player1 === 'rock'">Player 2
  wins!</p>
<p v-else-if="player2 === 'scissors' && player1 === 'paper'">Player 2
  wins!</p>



</template>

<script setup>
let user = "Laura"
let choices = ["rock", "paper", "scissors"]
let player1 = choices[Math.floor(Math.random() * 2)]
let player2 = prompt("rock, paper, or scissors?");

</script>


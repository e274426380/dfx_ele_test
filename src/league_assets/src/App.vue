<template>
  <div id="app">
    <div>{{ internetComputerGreeting || 'Loading message from Internet Computer...' }}</div>
  </div>
</template>

<script>
import { Actor, HttpAgent } from '@dfinity/agent';
import { idlFactory as league_idl, canisterId as league_id } from 'dfx-generated/league';

export default {
  data: () => {
    return {
      internetComputerGreeting: ''
    };
  },
  created() {
    const agent = new HttpAgent();
    const league = Actor.createActor(league_idl, { agent, canisterId: league_id });

    league.greet(window.prompt("Enter your name:")).then(greeting => {
      this.internetComputerGreeting = greeting
    });
  }
}
</script>

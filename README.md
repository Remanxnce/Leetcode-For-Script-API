# Leetcode for Script API

Wanting to learn the script API? wanting to just learn how to code? 
Hopefully, with Minecraft Bedrock's scripting API and the challenges 
I've made, you'll be able to gain a decent idea of how to code using 
the Script API.

## About

A lot of people recently have been asking me to help them learn how to code. While I don't mind helping people, I didn't want to do one-on-one teaching to people that I hardly knew.
So, my solution? create this. leetcode exists for people who want to learn how to code better, and while that applies to general code, some people lack the motivation or initial skils to learn code. My hope is that by making this, I'll be able to push people in the right direction with coding.

### What qualifies you?

- I was taught how to code by [THE BOSS](https://github.com/THEBOSS9345)
- I've been coding for about a year now.
- I've worked with the API and created a Bedrock Server, NEO PvP.
- I've worked with [Bedrock Protocol](https://github.com/PrismarineJS/bedrock-protocol) to create projects for private and independent use.
  - I'm currently making a private-use tickets bot!
- I have basic knowledge of HTTPS requests with the XBOX API. 

## Where are the challenges?

To view any of the challenges, head to the [challenges folder](https://github.com/Remanxnce/Leetcode-For-Script-API/tree/main/Challenges) and choose a challenge. They will all have a date of creation, a __Relative Difficulty__, and some hints posted.
 - Relative Difficulty is just a rating of how hard it is compared to some of the other challenges. these can change at any time.

## Cross Communication

Just to show how a challenge might be done, the solution for [Health-Displays](https://github.com/Remanxnce/Leetcode-For-Script-API/blob/main/Challenges/cross-communication.md) will be posted below.

```js
import {world, system} from "@minecraft/server"

system.runInterval(()=>{
    for (const player of world.getAllPlayers()){
        const health = player.getComponent(`health`)
            const maxHP = health.effectiveMax
            const currentHP = health.currentValue

        player.nameTag = `${player.name}\n§c${currentHP}/${maxHP}`
    }
})

```
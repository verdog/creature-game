# `creature game` design document

## description

`creature game` is a game about observing a world populated by procedurally generated creatures. the player will not have very much direct control of the game world, but will have some indirect control in the form of altering creatures' stats and abilities. the creatures and world will continue to operate while the player is gone. 

the game is meant to be something that is checked on once in a  while, rather than actively played for a long period of time.

## version history

```
1.0 | jan 7th, 2020 | initial draft
```

## index

```
- characters and story
    - characters
    - story
    - theme
- gameplay
    - goal
    - mechanics
        - creature behavior
        - evolution and species
        - world exploration
        - world progression
        - world reset
- art style
- music and sounds
- technical description
- misc ideas
```
---

## characters and story

### characters

the only characters in `creature game` are creatures. creatures are a part of a species. creatures within the same speicies exhibit mostly the same traits as other creatures in the same species, with only slight variations.

there are multiple species in the game world. a core part of the game will be the constant generation of new species.

a new species is periodically randomly generated and put into the game world. the first player to discover a species has the opportunity to name the species. the player also has the freedom to influence how the species evolves and what traits it has or will gain.

### story

there isn't much story to `creature game`. however, one element that might be considered a story element is the fact that the game world will be completely reset every once in a while to give everyone and everything a fresh start.

### theme

the game will have a theme of being small in a large world. the player can only gently nudge the game world and watch what happens.

## gameplay

### goal

the game does not have any concrete goal or built-in way to win. the game is more of a simulation which the player will check on every once in a while.

### mechanics

#### creature behavior

creatures will behave based on neural networks unique to a creature's species. the neural network will determine their actions and survival strategies. species start with a randomly generated neural network. players will be able to inspect a creature and see a visual representation of its network brain.

#### evolution and species

the main focus of `creature game` is to watch as a world starts with many species and, over time, dominant species take over and evolve. over time, species with advantagious neural networks will natually have an easier time surviving in the game world and start to populate it. every time a creature reproduces, the two parents pass on half of their networks each, with a chance for mutations to occur.

the overall behavior will be heavily influenced by the methods discussed in this paper:
http://nn.cs.utexas.edu/downloads/papers/stanley.ec02.pdf

species in the game world will be those derived from starting species and also randomly created new species.

#### world exploration

the main task of the player will be to explore the game world looking for interesting creatures. if a player is the first to stumble upon a creature in a species, they will be able to name the species and customize its appearance to their liking.

#### world progression

as the methods required for the neural network evolution to work require a lot of time, the game will alternate between two speeds:

1. real time speed, where the world updates in real time and is observable to the player
2. fast speed, where the game is inaccessable to players and is purely simulating the advancement of time. this is required to speed of the rate at which interesting and capable species of creatures emerge from the noise.

#### world reset

every so often, the world will be completely reset as to allow a completely new set of species to emerge.

with a world reset comes new terrain generation.

---
## art style

the game will be 2d in a slightly high resolution pixel art style. an emphasis is placed on bright and engaging visuals since the actual gameplay isn't very engaging.

## music and sounds

the game will have no music and a minimal amount of sound. the game is meant to be played as something you check up on every once in a while and should be mostly unintrusive. there should be no instances where the use of sound is required, and the game will start muted.

## technical description

the game will run in a browser. the browser will act as a client which communicates with a server back end which does all the number crunching.

for version control, the game's client and server history will be managed in a git repository.

the version control repository will not contain the art and music of the game. art and music will be stored seperately.

## misc ideas

- the player could have a private world where they could save creatures they particularly liked

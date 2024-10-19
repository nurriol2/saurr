# _Saurr!_

_Saurr!_ is a Pokémon team planner for the single-player experience.

_Saurr!_ works by modeling everything in the game as a [mathematical graph](https://en.wikipedia.org/wiki/Graph_theory)
and running a program to look through nodes of the graph that match a list of
Pokémon.

I talk more about how _Saurr!_ works on [my blog](https://elliotsmaker.space/).

## Background

I used three different websites to plan a team to use in the single-player story
of Pokémon Crystal Version.

I thought it was strange that I didn't find an all-in-one tool to plan a
single-player team.

But, Pokémon team planners usually assume that the user is building a competitive
team for a player-versus-player Pokémon battle.

So these planners show information that is useful for competition, like
a team's weaknesses or a Pokémon's moveset.

Sadly, I'm not very interested in competitive Pokémon. So, most of this
stuff is ignored.

I'm much more interested in info like the locations of each Pokémon on my
team, any prerequisites to catch them, and the earliest point that each Pokémon
is available.

I haven't found a team planner that addresses these single-player concerns, yet.

If you know of one, please email me at elliotsmakerspace@gmail.com so this file
can be updated.

For now, I built _Saurr!_ to meet these needs and automate the planning process
with a single tool.

## Features

- Support Generation 1 - 3 games
- Support multiple languages
- Automatically check for version exclusive Pokémon
- Build a guide for the single-player story based on a list of chosen Pokémon
- Save guides in a [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github) file
- Save lists of teams in a [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github) file
- Write notes about each team
- Application available as a command line utility
- Application available on the web

### Web Exclusive Features

- Graph searching animation
- Shareable team URL

## Installation

1. Clone this repository

```
git clone git@github.com:nurriol2/saurr.git
```

2. Move into the newly created directory

```
$ cd ~/path/to/saurr/

$ pwd
/home/<user>/path/to/saurr
```

### Web

Use the web app [here](https://<TODO>.deta.dev)

## Usage

### CLI

General usage:
`$ python saurr.py [OPTIONS] <TEAM_ID> [ARGS]`

Look up a team by its ID - in this case `TEAM_A`

```
$ python saurr.py TEAM_A

$ |--------------|-----------------------|
$ |  TEAM_A      | Notes                 |
$ |--------------|-----------------------|
$ |  Crystal     | - First Playthrough   |
$ |--------------| - Casual team         |
$ |  *Roster*    | - Here's another note |
$ |--------------|                       |
$ | 1. Venusaur  |                       |
$ | 2. Dugtrio   |                       |
$ | 3. Dodrio    |                       |
$ | 4. Primeape  |                       |
$ | 5. Starmie   |                       |
$ | 6. Ninetails |                       |
$ |--------------|-----------------------|
```

Create a new team named `TEAM_B`

```
$ python saurr.py --new TEAM_B

$ Created a new team at TEAM_B
```

Pick a game - in this case Pokémon `Crystal` Version

```
$ python saurr.py --game TEAM_B Crystal

$ TEAM_B is now using the (Gen. 2) Pokémon Crystal Version Pokédex
```

Add Pokémon to `TEAM_B`

```
# Add a single Pokémon
$ python saurr.py --add TEAM_B Hitmonlee

$ Added Hitmonlee to TEAM_B

# Add more than one Pokémon
$ python saurr.py --add TEAM_B Krabby Meganium Spinarak

$ Added Krabby, Meganium, and Spinarak to TEAM_B

```

Delete Pokémon from `TEAM_B`

```
# Delete a single Pokémon
$ python saurr.py --del TEAM_B Hitmonlee

$ Deleted Hitmonlee from TEAM_B

# Delete more than one Pokémon
$ python saurr.py --del TEAM_B Krabby Meganium Spinarak

$ Deleted Krabby, Meganium, and Spinarak from TEAM_B
```

Get help or see all the available options
`$ python saurr.py --help`

### Web

TODO: Add screenshots mirroring CLI Usage

## Contributing

Not currently taking contributions.

_Thank you for your time and attention, but Saurr! is not currently taking_
_contributions._

_If you clone this repository and make something all your own, I would love_
_to hear about it! Email me at:_

_elliotsmakerspace@gmail.com_

## License

[MIT](https://choosealicense.com/licenses/mit/)

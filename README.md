# NewLife2

> _Scripting the birth of a new life._

NewLife2 is a [KoLmafia] script that automates common tasks whenever you start a new ascension.

NewLife2 is a fork of [newLife] ([repository](https://sourceforge.net/projects/new-life.bale.p/)), which was written by [Bale].

## What is this?

Whenever you ascend in Kingdom of Loathing, you need to perform a variety of common tasks. You will also want to reconfigure KoLmafia to pick the best choice for your class and path in various non-combat adventures. Doing this every ascension can become tedious.

NewLife2 automates these tasks for you. It does:

- Perform various post-ascension tasks, such as visiting the Toot Oriole
- Prepare your inventory, such as unpacking astral consumables, taking free pull items from Hagnk's, etc.
- Pick "optimal" choices for various choice adventures
- Optimize KoLmafia's auto-recovery settings for your class and path
- If you have enough skill points to learn all skills in an Avatar path, unlock them all immediately

...and more!

## Installation

To install NewLife2, enter the following in the KoLmafia gCLI:

```
svn checkout https://github.com/Loathing-Associates-Scripting-Society/newlife2/trunk/release/
```

To make KoLmafia automatically run NewLife2 upon ascension, enter:

```
set postAscensionScript = newlife2.ash
```

When you are done, you can remove Bale's newLife:  
(_Note: If you have multiple KoL accounts, check if none of them are using newLife before doing this!_)

```
svn delete bale-new-life
```

## Configuration

NewLife2 can be configured using [ZLib]. It supports all variables originally used by newLife. (_Note: This may change in a future version of NewLife2._)

To set a variable, enter:

```
zlib <variable name> = <value>
```

All variable names and values are case-sensitive.

- `newLife_SellPorkForStuff`
  - Allowed values: `true` (default), `false`
  - If set to `true`, NewLife2 will autosell _some_ of your pork gems in order to acquire enough meat for a [detuned radio], [toy accordion], etc. If set to `false`, NewLife2 will not attempt to buy such items at all.
- `newLife_SmashHippyStone`
  - Allowed values: `true`, `false` (default)
  - If you want NewLife2 to smash your [Magical Mystical Hippy Stone], set this to `true`.
- `newLife_SetupGuyMadeOfBees`
  - Allowed values: `true`, `false` (default)
  - Normally, NewLife2 will not call for [The Guy Made of Bees] in the Haunted Bathroom. If you like to set up the GMoB, set this to `true`.
- `newLife_UseNewbieTent`
  - Allowed values: `true` (default), `false`
  - If set to `false`, NewLife will not set up a [Newbiesport&trade; Tent] at your campsite, which allows other people to [brick] your face.

### Deprecated Configuration Variables

The following variables are deprecated, and may be removed in a future version:

- `newLife_Extras`
  - Allowed values: `true`, `false` (default)
  - If set to `true`, NewLife2 will perform some tasks differently and in an opinionated way.  
    Note: This was implemented by Bale for their personal use.
  - Changes include, but are not limited to:
    - If in softcore, no longer announces "brick me" messages in the **/clan** chat channel
    - Unlock [Zombie Slayer] skills even if you don't have 30+ skill points
    - Prepare some IotMs, e.g. Xiblaxian stuff
    - Pull and equip some IotM equipment
  - For more details, please refer to the source code.

[bale]: https://github.com/balefull
[brick]: https://kol.coldfront.net/thekolwiki/index.php/Brick
[detuned radio]: https://kol.coldfront.net/thekolwiki/index.php/Detuned_radio
[kolmafia]: https://kolmafia.us/
[magical mystical hippy stone]: https://kol.coldfront.net/thekolwiki/index.php/Magical_Mystical_Hippy_Stone
[newbiesport&trade; tent]: https://kol.coldfront.net/thekolwiki/index.php/Newbiesport%E2%84%A2_Tent
[newlife]: https://kolmafia.us/threads/scripting-the-birth-of-a-new-life.2769/
[the guy made of bees]: https://kol.coldfront.net/thekolwiki/index.php/Guy_Made_Of_Bees
[toy accordion]: https://kol.coldfront.net/thekolwiki/index.php/Toy_accordion
[zlib]: https://kolmafia.us/threads/zlib-zarqons-useful-function-library.2072/
[zombie slayer]: https://kol.coldfront.net/thekolwiki/index.php/Zombie_Slayer

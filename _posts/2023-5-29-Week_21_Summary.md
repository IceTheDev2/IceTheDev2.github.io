---
layout: post
title: 29 May 2023, Week 21 Summary
---

PASSWORDSY: https://github.com/IceTheDev2/Passwordsy/releases

LIGHT GAME:
- GitHub (Source Code): https://github.com/IceTheDev2/light-game/releases
- itch.io (Download): https://icethedev2.itch.io/light-game

## SUMMARY OF THE 22 - 28 MAY WEEK

### MONDAY, 22 MAY:
- [Fixed the text updating bug in light game beta-1.1.](https://github.com/IceTheDev2/light-game/releases/tag/beta-1.1)
- [Fixed the password strength checker warnings freeze in Passwordsy v2.3.1-beta.](https://github.com/IceTheDev2/Passwordsy/releases/tag/v2.3.1-beta)
- Cleaned Passwordsy code.
- [Added level 1 to light game, featuring a triangle enemy and some explanation on its behaviour](https://github.com/IceTheDev2/light-game/releases/tag/beta-1.2).

### WEDNESDAY, 24 MAY:
- [Fixed the health showing 1 when dead bug in light game beta-1.2.1.](https://github.com/IceTheDev2/light-game/releases/tag/beta-1.2.1)

### THURSDAY, 25 MAY:
- [Added support for Linux and Android, alongside Windows, in light game beta-1.3.](https://icethedev2.itch.io/light-game/devlog/536184/beta-13-support-for-windows-linux-and-android)
- Updated itch.io theme to match my logo’s colours.
- Added levels 2 and 3 to light game.
- [Implemented @‌kevintr303’s idea of an infinite level (beta-2.0).](https://icethedev2.itch.io/light-game/devlog/536335/beta-20-added-infinite-level-feature-by-kevintr303)

### FRIDAY, 26 MAY:
- Wrote a blog post about changing an object’s colour.
- Fixed 3 light game bugs: Button animations weren't showing when clicking fast in previous versions. This has been fixed by adding a delay to wait for the animation to end after clicking the button before executing the button's code. Fixed the animation of the Infinite Level button (is used to take 0.25 secs to look pressed, now it's instant, like all the others). Fixed the bug where the game wouldn't be even although the player's light would collide with the green square (because the collision has started before the win delay passed), by changing from OnCollisionEnter2D to OnCollisionStay2D.
- [Triangles no longer avoid the square in light game beta-2.4.](https://icethedev2.itch.io/light-game/devlog/536672/beta-24-triangles-no-longer-avoid-the-square)
- [The Infinite Level button is now centered.](https://icethedev2.itch.io/light-game/devlog/536729/beta-241-centered-infinite-level-button)

Hopefully this week will be more productive.

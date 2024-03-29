# Overview

Have you seen the enviro-suited intensity of Silfae's "Animated Quarian Portraits" mod?  Do you wish that the gameplay elements were up-to-date so that you can play the Migrant Fleet or make a new species of interstellar wanderers?  Then this mod is for you!

There are lots of other mods which contain the same or similar portraits, so why should you choose this one? Silfae's art style meshes well with Stellaris, or maybe you want to play her version of the Migrant Fleet - content which this mod again makes playable.  Please enjoy my translation of Silfae's custom empire into modern Stellaris.

# Changes

All gameplay features from the original mod are upgraded to be fully compatible with Stellaris 3.8 "Gemini," the latest version when this was written.  Updates include:

* Fix invalid texture reference in `quarian_female_01_portrait.mesh` (caused lots of error logs)
* Improve Quarian clothing selectors to be influenced by Pop job
* Update the namelist to account for all built-in army types, remove obsolete entries; Army names more lore-friendly
* Update custom starting initializer
    * Original version with a habitable planet
    * New version that works with the Void Dwellers origin (available for any Void Dwellers)
* Add custom trait "Wanderers" that is a higher-powered version of Nomadic: +30% growth from immigration, -50% resettlement cost, +50% pop automatic resettlement chance
* Replace original "Quarian" trait with "Immunocompromised" that gives +5% engineering research, -5% habitability (0 points) - available for any species (AI will not use it)
* Update pre-scripted empire
    * Now has oligarchic authority to reflect Quarian government style
    * Now has Origin: Void Dwellers (requires Federations)
    * Species traits altered: Void Dwellers, Wanderers, Intelligent, Immunocompromised, Nonadaptive, Deviants (selected based on the effects of Silfae's original design)
    * Starting leader begins with three traits: Home in the Sky, Space Miner, and Fleet Organizer
    * Can randomly spawn
* You can use the Quarian portraits for your own empire without any DLC requirements
* The Quarians are part of the Humanoid species class (since Stellaris 3.8)
* Support being able to choose a single-gender species (since Stellaris 3.2)

## Compatibility

In order to add a new solar system initializer that is compatible with Void Dwellers, it is necessary to override `origin_void_dwellers` add it to the list of allowed initializers.  That means this mod is incompatible with other mods that modify that origin definition, such as other mods that add new initializers for Void Dwellers.

Compatible with any other mod that does not add the same portraits or art assets.

The Launcher will tell you that some mods are outdated - that is because the dependency is out of date with the game's version number.  This mod overwrites and replaces all incompatible code so that the portrait mod will function as originally designed.  You can safely ignore the out-of-date warning for the dependency mod.

Built for Stellaris version 3.8 "Gemini."  Not compatible with achievements.

### Dependencies

In order for this mod to function, you **must** install the following mod and load it before this one:

[Animated Quarian Portraits](https://steamcommunity.com/sharedfiles/filedetails/?id=708669421) by Silfae

### Recommended Companion Mods

[Migratory Fleet](https://steamcommunity.com/sharedfiles/filedetails/?id=2531002116) if you want to play as an actual fleet instead of using habitats. I am not involved with the development of this mod, however it is very impressive what the author achieved within the limits of Stellaris.

### When to Install

This mod should be added before the game has started.  If you remove it from a game in progress, your game may have graphical problems if any species was using the custom portraits.

## Known Issues

Silfae's original mod does not include graphics for ecumenopoleis, so they will fall back to the Mammalian graphical culture. If anyone knows of a mod that provides said stage-6 city picture, I would be happy to investigate getting permission to reuse the graphics, or add it as a dependency to this one.

This mod overrides `origin_void_dwellers` in order to add its new initializer to the allowed list, which generates an error like this:

```
[23:27:16][game_singleobjectdatabase.h:165]: Object with key: origin_void_dwellers already exists, using the one at  file: common/governments/civics/05_quarian_revisited_origin_overrides.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.0.1 Add second set of random species names, ensure original file is overwritten
* 1.0.2 Tweak namelist
* 2.0.0 Update for compatibility with Stellaris version 3.1 "Lem"
    * Add new localisation keys introduced in 3.1
    * Update override of `origin_void_dwellers` to reflect additional base game restrictions (no Idyllic Bloom)
* 3.0.0 Update for compatibility with Stellaris version 3.2 "Herbert"
    * Apply new mono-gender portrait rules
    * More Pop clothing selector refinements
    * Update override of `origin_void_dwellers` to reflect additional base game restrictions (no Anglers)
* 3.0.1 Don't break the base game diplomacy rooms - fix is to name the new file to load _before_ the built-in file
* 3.0.2 Minor tweaks
    * Portrait selectors based on job category, not pop category - my goal is for the Pop portraits to be based on the job, not the Pop's stratum
    * No longer ignore portrait duplication for the pre-scripted empire
* 4.0.0 Update for compatibility with Stellaris version 3.3 "Libra"
    * Integrate base game script changes
    * Use a shared set of triggers for job-based clothing
* 5.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Update shared triggers
    * Add slave cost to a custom trait
    * All static text moved to localisation (name lists, species random names, prescripted empire)
* 6.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Minor namelist updates
    * Update `hair` to `attachment`
    * Quarian attachments are labeled "Mask"
    * Update Wanderer trait to work with new gene-modding
    * Ensure overridden Void Dwellers origin is up-to-date
* 7.0.0 Update for Stellaris version 3.7 "Canis Minor"
    * Update shared triggers for Pop portraits
    * Remove global flag
    * Add compatibility trigger `has_quarian_portraits_revisited_active`
* 7.0.1 Fix compatibility scripted trigger to have the right name
* 8.0.0 Update for Stellaris version 3.8 "Gemini"
    * Quarians are now part of the Humanoid species class (thanks to changes by Paradox, this is no longer mod-unfriendly)
    * Update prescripted empire to use the new prescripted ruler class and trait system
    * Update shared triggers

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/quarian_portraits_revisited)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.

# Special Thanks

I was inspired to extend the original mod when I saw [Endugu](https://steamcommunity.com/profiles/76561198037630876/myworkshopfiles/)'s [expansion](https://steamcommunity.com/sharedfiles/filedetails/?id=1584824947) of [Silfae](https://steamcommunity.com/profiles/76561198021525667/myworkshopfiles/)'s [Animated Xirmian Portraits](https://steamcommunity.com/workshop/filedetails/?id=881118424).  Modular mods that require downloading the original mod(s) help give credit where credit is due.

An extra special thanks to Silfae for creating and sharing so many detailed, animated portraits for the community.
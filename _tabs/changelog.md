---
layout: post
icon: fa-solid fa-list-ul
order: 12
toc: true
---
<style>
.yellow {
color:rgba(255, 194, 41, 0.5);
}
</style>

<hr>

## <span class="yellow">[2.1.1.1] (1.20.1) 2023-12-07</span>
### Changes
- Updated minimum Geckolib version to 4.3.1

## <span class="yellow">[2.1.1] (1.19.2 | 1.20.1) 2023-11-28</span>
### Fixes
- Fixed compatibility with mods attempting to access spell names from the server
- (1.20.1) Fixed item cooldown rendering using the wrong coordinate
 
## <span class="yellow">Eldritch Update [2.1.0] (1.19.2 | 1.20.1) 2023-11-26</span>
### Additions
- Added New School, Eldritch
  - Spells
    - Added Planar Sight Spell
    - Added Sonic Boom Spell
    - Added Telekinesis Spell
    - Reenabled Abyssal Shroud Spell
    - Reworked Sculk Tentacles Spell (was Void Tentacles)
  - Items
    - Added Eldritch Manuscript Item
    - Added Ancient Knowledge Fragment Item
  - Research System
    - Eldritch Spells are unlearned by default. (Cannot be crafted nor cast)
    - Added Research Menu, accessed by Eldritch Manuscripts
- Misc
  - Added Divine Smite Spell
    - This spell is always uninterruptible
  - Added additional Wandering Trader trades
    - Sell ink to Wandering Trader
    - Buy Curios from Wandering Trader
    - Buy scrolls from Wandering Trader
    - Buy mystery bags of scrolls from Wandering Trader
    - Buy Ancient Knowledge Fragments from Wandering Trader
  - Added a Patchouli page for Schools
  - Added a learnSpell command
  - Added Ukrainian Translations
  - Added inherent mob spell resistance
    - Undead are weak to Holy magic and resistant to Blood magic
    - Fire mobs are resistant to Fire magic
    - Water mobs are weak to Lightning magic
  - Added Scroll Bar to Scroll Forge

### Changes
- Spell Balance
  - Ice Block Spell now moves faster and initiates its fall sooner
  - Counterspell Default cooldown reduced from 15s -> 10s (existing worlds need config reset)
  - Improved Lightningbolt Spell's hit detection/placement
  - Increased Lightning Lance Spell's Damage
  - Decreased Lightning Lance Spell's Default Rarity from Rare -> Uncommon (existing worlds need config reset)
  - Magma Bomb impact damage no longer scales with spell level
  - Magma Bomb aoe damage slightly increased
  - Magma Bomb radius is reduced, and now scales with spell power
  - Gust Spell is less affected by knockback resistance
- Misc
  - Unique Spell Books can have their spells improved in the Arcane Anvil, by combining it with a higher level scroll
  - Evoker Spell Book now gives +10% Evocation Spell Power
  - Improved animation smoothing
  - Updated Chinese Translations

### Fixes
- Fixed Spell Power and Resistance Attributes not being able to go below 1
- Fixed Fireward Ring strange behavior due to reliance on mob effect

### API
- Spells now have methods for crafting criteria, craftability, lootability, and interruptibility
- Consolidated mana and cooldown checks into a CastResult class
- Added canBeCastBy (returns CastResult) method to AbstractSpell

## <span class="yellow">[2.0.3] (1.19.2 | 1.20.1) 2023-10-29</span>
### Fixes
- Removed accidently left-in testing code that could mess with mana

## <span class="yellow">[2.0.2] (1.19.2 | 1.20.1) 2023-10-28</span>
### Additions
- Added Mana Regen attribute
- Added the Amethyst Resonance Charm, a craftable necklace that gives +15% mana regeneration

### Changes
- Buff Magic Arrow's base damage by 5
- Add CastSource to SpellCastEvent for developers
- Rework Priest Armor Texture, courtesy of Crydigo
- Tweak most jewelry textures
- Any armor can now be upgraded instead of only mage armor (can_be_upgraded tag has been removed)
- Spectral Hammer debris reduced

### Fixes
- Fixed inconsistent Magic Arrow block penetration
- Fixed the two-handed sword models when using left hand mode
- Mobs can no longer detect your armor when affected by True Invisibility
- Fixed geckolib armor anchor points causing misaligned armor models when the player is animating
- Fixed JEI recipe autocomplete exploit
- Fixed Raise Dead spell not being able to find suitable ground locations at y < 0

### API
- Added InscribeSpellEvent, courtesy of Silvertide7
- Added ChangeManaEvent
- Added SpellDamageEvent

## <span class="yellow">[2.0.1] (1.19.2 | 1.20.1) 2023-10-02</span>
### Additions
- Added SpellCastEvent and SpellHealEvent for developers, courtesy of Silvertide7

### Changes
- Significantly Optimized WorldUpgrader by skipping uninhabited chunks

### Fixes
- Fix Alchemist Cauldron having a null level when spawned in as a structure

## <span class="yellow">Spell Registration Update [2.0.0] (1.19.2 | 1.20.1) 2023-09-24</span>
### Additions
- New Spells
  - Added Earthquake Spell
  - Added Ray of Frost Spell
  - Added Summon Ender Chest Spell
  - Added Firefly Spell
  - Added Oakskin Spell
- Added Elixirs
  - Added Oakskin Elixir
  - Added Invisibility Elixir
  - Added Evasion Elixir
  - Added Greater Potion of Healing
- Added Firefly Jar block
- Added the Druidic Tome, an epic Nature spell book 
- Added spell targeting success notification
- Added school based resistance attributes
  - While these are not used in the game yet, they can be used by modpacks or addons

### Changes
- Schools
  - Poison School has been replaced by the Nature School
  - Void school has been temporarily removed while it is being reworked
    - Black Hole is now an Ender spell
    - Void Tentacles is now an Ender spell
    - Abyssal shroud is now disabled by default (configurable)
- Spells
  - Devour spell no longer pulls enemies in, and has had its range extended
  - Long casts can no longer be held to cast
  - Long casts must be clicked again to cancel mid-cast
- Mobs
  - Cryomancer, Pyromancer, and Archevoker max health increased by 10
  - Cryomancer, Pyromancer, Archevoker, and Necromancer will now attempt to flee from melee combat
  - Archevoker will now use the Gust spell
  - Increased Arcane Essence drop quantity from the Necromancer
- Textures
  - Updated Anicent Codex, Enchanted Spell Book, and Grimoire of Evokation textures
  - Updated Inscription Table's Lore Page texture
  - Update Amulet of Concentration's texture
  - Updated Wandering Magician, Priest, and Electromancer Chestplate icons to better match their armor model
- Misc
  - Potions can now be put into the Alchemist Cauldron
  - Ink can now be put into the Alchemist Cauldron
  - Ink can now be upgraded in the Alchemist Cauldron
  - The visuals of the Target Area Outline (used in spells like Healing Circle) have been improved

### Fixes
- Fixed an issue causing casting mobs to have a difficult time teleporting around non-flat terrain
- Fixed input issues caused by hybrid long casting inputs
- Fixed Cyromancer's armor attribute not reflecting his worn armor

## <span class="yellow">[1.2.1] (1.19.2 | 1.20.1) 2023-08-10</span>
### Additions
- Added the Decrepit Flamberge sword
- Added error message to the Wayward Compass if there is no found structure

### Changes
- Slimmed down Electromancer Chestplate Model
- Slimmed down Priest Chestplate Model
- Slimmed down Archevoker Chestplate Model
- Removed Black Pixel from Archevoker Shoulderpad
- Updated Archevoker, Pyromancer, Electromancer, and Scarecrow Hat icons
- Updated Archevoker and Electromancer Chestplate icons to better match their models
- Slightly Tweaked Pyromancer Hat model
- Updated Plagued Helmet and Chestplate icons
- Overhauled Ancient Knight animations
- Overhauled Ancient Knight sounds
- Overhauled Ancient Knight energy layer
- Ancient Knights now carry Decrepit Flamberges
- Magehunter sword reworked
- Tweaked Chain Lightning and Healing Circle spell icons

### Fixes
- Fixed Black Holes of small enough radius causing a divide by zero crash

## <span class="yellow">[1.2.0] (1.19.2 | 1.20.1) 2023-07-29</span>
### Additions
- Added the Alchemist Cauldron
  - Allows for scrolls to be recycled into ink
  - Allows for brewing of 4 potions at once
  - Allows for production of Blood Vials
  - Supports interactions with dispensers, hoppers, and observers
- Added Mana Potion, which can be brewed from Arcane Essence
- Added loot integration to all of Yung's structure mods
- Added loot integration to Structory

### Changes
- Priests will now heal friendly players
- Aoe and Cone spells no longer cause knockback
- Instant cast spells no longer spam their cooldown error if right click is held down
- Some loot table rebalances, including ink now dropping outside of Iron's Spellbooks structures

### Fixes
- Fixed Aoe entities damaging summons and teammates
- Fixed Wall of Fire igniting summons and teammates
- Fixed True Invisibility effect icon disappearing

## <span class="yellow">[1.1.8] (1.19.2 | 1.20.1) 2023-07-17</span>
### Additions
- Added spell descriptions to tooltips in Inscription Table and Scroll Forge
- Added config option for the cooldown multiplier of imbued weapons
- Added entity collision to the Shield Spell
- Added JEI descriptions on how to obtain various materials

### Changes
- Updated Affinity Ring Textures
- Updated Arcane Cloth and Ingot Textures
- Level of Vigor gained from Devour Spell is now capped at level 10
- Fang Strike default fang count of increased by 2
- Fang Strike fangs now activate faster
- Fang Strike and Fang Ward base cast time reduced to .75 seconds
- Fang Ward fang count now increases exponentially with its ring count
- Imbued weapons now have half the cooldown instead of twice the cooldown
- Updated to new patchouli book format

### Fixes
- Fixed an exploit that could bypass a spell book's rarity limit when inscribing a spell (fixes #94)
- Fixed an exploit that allowed a different focus to be used to craft a scroll (fixes #100)
- Fixed some magic projectiles ignoring shield spell
- Fixed aoe damage sources damaging shields multiple times
- Fixed Magehunter not showing Counterspell until used
- Fixed casting mobs causing null crash if casting while dying

## <span class="yellow">[1.1.7] (1.19.2 | 1.20.1) 2023-07-06</span>
### Additions
- Added Amulet of Concentration

### Changes
- Redid Icicle Projectile Visuals
- Slowed Down Icicle Projectile
- Redid Icicle Spell Icon
- Redid Snowflake Particle Texture
- Redid Magic Missile Visuals
- Redid Magic Missile Icon
- Replaced Dead King Boss Model and Weapon Model, thanks to Crydigo. Includes Programmer Art Texture Pack

### Fixes
- Fixed Spellcasting Mobs casting Fang Strike while out of range
- Fixed Quick Casting a spell out of bounds of your current spell book causing a crash
- Fixed summoned horse being able to enter a glitched death state if summoned while dying
- Fixed the Dead King not using a second single use spell during his second phase
- Lightning Bolt Spell no longer strikes multiple times
- Fixed latest version of Forge causing loot modifiers to crash game

## <span class="yellow">[1.1.6] (1.19.2 | 1.20.1) 2023-06-26</span>
### Additions
- Added Devour Spell, patreon request of Yorhavich
- Added Patchouli Guide Book
- Added descriptions in JEI for Bottles o' Lightning and Blood vials for how to obtain them
- Added config for Priest House spawn rate

### Changes
- Combined Long and Charge Casts
- Made battlegrounds smaller and more rare
- Reworked Priest House to better fit vanilla and modded villages
- Priest shakes his head like a villager if you interact with him
- Refactored mana bar's hunger Y value calculation to automatically fit with other mods UI elements

### Fixes
- Fixed piglins in the battlegrounds not having weapons
- Chain Lightning can no longer target non-living entities, such as minecarts
- Ceased cancelling the use item finish event
- Magical Area of Effect entities are now affected by counterspell
- Fixed typo in language file causing guiding bolt and chaing lightning death messages to not appear


## <span class="yellow">[1.1.5] (1.19.2 | 1.20.1) 2023-06-20</span>
### Additions
- Added a holy spellcasting mob: the Priest. Spawns in a new house in plains villages.
- Added Guiding Bolt Spell
- Added Chain Lightning Spell
- Added Gust Spell
- Added functionality to modded and vanilla projectiles to pass through players with evasion, instead of thinking there was an impact
- Added Spellbook Category of Equipment to Apotheosis (Thanks to amo)
- Added Poison Apotheosis Gem

### Changes
- Invisibility removes you as the active target from nearby mobs that were targeting you.
- Slimmed down priest armor model.
- Disabled first person animations entirely if both configs are disabled
- Improved casting mob movement logic

### Fixes
- Scroll Forge Ink Outline shifted to match ink texture
- Fixed ground detection that prevented certain spells from working below y = 0
- Fixed and issue where casting mobs could choose to drink a potion and cast a spell at the same time


## <span class="yellow">[1.1.4] (1.19.2 | 1.18.2) 2023-06-08</span>
### Changes

- Updated Counterspell to counter magical effects that were recently added
- Update Scroll Forge ink outline to match new textures
- Shifted all ink textures 1 pixel to the right
- Removed Dismount message when rooted
- Improved mob teleport collision detection

### Fixes

- Target Area Visuals no longer persist if the owner dies while casting
- "None Spell" is no longer craftable
- Fixed Single Use Spell timer improperly being ticked, resulting in some mobs never casting it
- Fixed Crash when attempting to slot a spell into a full spellbook
- Fixed some spells not serializing damage

<hr>


## <span class="yellow">[1.1.3, 1.19.2] 2023-05-31</span>
### Changes
- Replaced ink, hogskin, dragonskin, and most spell book textures (Courtesy of Crydigo)
- Increased spell power bonus from 2.5% to 3% on school armor
- Increased spell power bonus on upgrades from 2.5% to 3% per upgrade
- Increased spell resistance upgrade bonus from 2.5% to 6%
- Increased cooldown upgrade bonus from 5% to 6%
- Update Chinese Translations

### Fixes
- Fixed playeranimator not displaying dependencies screen when the game was launched without it
- Fixed necromancer accidentally having only 1 spell

<hr>

## <span class="yellow">[1.1.2] 2023-05-27</span>
### Changes
- Ray of Siphoning render overhaul
- Firebolt render overhaul
- Fireball render overhaul
- Replaced vanilla fireballs with new fireball model (configurable)
- Added School to a spell's configuration
- Added client config for hiding mana bar text
- Added Fire Bomb, Starfall, and Healing Circle Spells
- Cloud of Regeneration is now disabled by default (won't take effect in preexisting world, reset your serverconfig)
- Added Affinity Rings, which give + 1 level to a random spell
- Added item model override support to scrolls and affinity rings
- Replaced all ring textures (thanks to crispytwig)
 
### Fixes
- Fixed Ancient Knight rendering at improper scale and color with shaders
- Fixed Dead King teleport collision check
- Fixed casting mobs improperly tracking aggression
- Fixed imbued weapon overlay not disapearing after dropping imbued item
- Fixed casting mobs being able to reuse a single use spell if the player relogs or goes out of combat
- Added null check to tooltip renderer

<hr>

## <span class="yellow">[1.1.1] 2023-05-19</span>
### Changes
- Updated Chinese Language File
- Renamed Poison Breath to Poison Spray (No other changes)
- Adjust Black Hole cast animation
- Reduced default max level of blight from 10->8 (will not take effect in preexisting worlds)
- Increase Aspect of the Spider default cooldown from 35s->90s (will not take effect in preexisting worlds)
- Added Blood Needles Spell
- Added Acupuncture Spell
- Increased Ray of Siphoning lifesteal rate from 35%->100%
- Increase Blood Slash lifesteal rate from 10%->15%
- Updated Spell Descriptions to include lifesteal rate
- Added error message if you try to cast a targeted spell with no target
- Redid Void Tentacles texture, also fixing shaders issue with the previous texture
- Redid Void Tentacle spell icon
- Fixed Spell Book Advancement Chain and added Dragonskin Spell Book to the chain

<hr>

## <span class="yellow">[1.1.0] 2023-05-12 - Poison Update</span>
### Changes
- New School Added: Poison
  - Corresponding Rune, Upgrade Orb, and Armor (The Plagued Armor Set)
  - Poison Breath Spell
  - Poison Arrow Spell
  - Poison Splash Spell
  - Acid Spit Spell
  - Aspect of the Spider Spell
  - Blight Spell
  - Root Spell
- Evoker Fort reworked:
  - Removed Library Floor
  - Decreased Spawn Rate
  - Moved loot to be harder to grab without fighting anything 
  - Known Issue: Captured Villagers do not adopt the biome of where they spawn
- Spell Balance Changes:
  - All "basic attack" spells deal more damage at lower levels, and less damage at higher levels
  - All cone spells have reduced damage scaling
  - Most "advanced attack" spells cooldown reduced
  - Shield is now larger, has significantly increased health, and can cast farther away from the player
- Loot Table Changes:
  - Reduced Vanilla Chest Scroll Drop chance
  - Increased rune drop chance in nether chests
  - Increased rune drop chance in catacombs chests
  - Increased rune drop chance in treasure chests
  - Reduced ink drop rates overall
  - Ink now drops from killing wizards and the dead king
  - Corresponding runes now drop from wizards
- General Changes:
  - Extended All Summons duration to 10 minutes instead of 3
  - Reworked Dragon Breath Pools
  - Continuous Tooltips are now in mana per second
  - Tooltips say charge time instead of cast time for charge casts
  - Teleports can now go through water
  - Added Mana command
  - Added Poisonward Ring (immune to poison)
  - Wizards now drink potions instead of spamming heal spell
  - Necromancer Spawn Rates significantly reduced
  - Rebalanced the spell arsenal of the necromancer, archevoker, cryomancer, and pyromancer
  - JEED Support
  - Apotheosis Initial Support (more to come)
  - Ascension now charges creepers
  - New Void Spell
  - Cryomancer in Mountain Tower now guards the loot instead of being useless at the top of the tower
  - Ancient Knights are now immune to fall damage and fire damage, and will lunge more frequently
  - Added Shriving stone, which can remove imbuements or upgrades in the smithing table
  - Increased Copper, Iron, and gold spell book capacity by 1 (will not take effect on old spell books)
  - Decreased Villager Bible Rarity to epic
  - Added new legendary spell book, the Dragonskin Spellbook (+10% Ender Power). Crafted From Dragonskin, a new ender dragon drop
  - Added Dragonskin
  - Gave +20% cooldown reduction to the Ancient Codex

### Fixes
- Fixed precast sounds sometimes playing at the wrong time on the client
- Fixed Missing pixels on Cultist and Priest Armors
- Fixed Client duplicating teleport particles
- Fixed Broken Inscription Table generation in mountain tower

<hr>

## <span class="yellow">[1.0.9] 2023-05-12</span>
### Changes
- Added new Mana UI config (Anchoring, Display mode, and XP mode)
- Casting errors moved from chat onto the action bar
- Generified imbuement and added imbuement config overrides, so you can now imbue anything

### Fixes
- Fixed additional dimensions causing mana regen issues
- Made rarity config thread-safe to actually prevent another REI related issue
- Fixed Summon Timer effect not immediately syncing to client after player respawn

<hr>

## <span class="yellow">[1.0.8] 2023-05-06</span>
### Fixes
- Hotfix to make loading rarity config thread safe to prevent an REI related crash

<hr>

## <span class="yellow">[1.0.7] 2023-05-03</span>
### Changes
- Summons now show death and despawn messages to their owner
- Summons now actively track their number through the pre-existing timer effect (mouse over in inventory to see how many are remaining)
- Summons now remove their effect timer if all summons are dead
- The summon effect timers are not wiped after player death
- Added summon damage attribute, which increases your active summon's damage
- Added Conjurer's Talisman, a necklace that gives +10% summon damage
- Increased Summoned Polar Bear's speed
- Summons and Tamed Animals can no longer agro each other
- Reworked fog particle to be significantly more visually appealing (currently only used in the Void Tentacle spell)

### Fixes
- Fixed a bug where summoned skeleton arrows could anger other summons
- Fixed Summoned Polar Bear not letting the player on after the player dies and respawns
- Fixed Black Pixels appearing around certain spells with some visual mods/shaders
- Fixed the tree half of the Evoker Fort being able to clip into the ground
- Fixed invalid rarity config entries being able to crash the game when looking at a tooltip

<hr>

## <span class="yellow">[1.0.6] 2023-05-03</span>
### Fixes
- Replaced most textures that used vanilla textures. This caused issues with texturepacks, especially ones using Optifine. While this does not extend compatibility for these texture packs, it alleviates conflict with them.

<hr>

## <span class="yellow">[1.0.5] - 2023-05-02</span>
### Fixes
- Fixed Dedicated Server Startup Issue https://github.com/iron431/Irons-Spells-n-Spellbooks/issues/15

<hr>

## <span class="yellow">[1.0.4] - 2023-05-01</span>
### Changes
- Added Spawn eggs for the Archevoker, Necromancer, Cryomancer, Pyromancer, Ancient Knight, and Dead King
- Added conflig for Mana Bar position offset in client config
- Added Tetra Material Support
- Arcane Ingot (metal, gives mana)
- Arcane Cloth (fabric, gives cooldown reduction)
- Hogskin (skin, gives new mana siphon effect)
- Runestones (socket, gives corresponding spell power)
- Frozen Bone (bone, gives freezing effect)
- Added Chinese Language Support (Thanks LILPRINCES)

### Fixes
- Improved Mangrove hut placement fix
- Cleaned up summoned entities, fixing https://github.com/iron431/Irons-Spells-n-Spellbooks/issues/8
- Fixed empty spell wheel log spamming
- Slightly tweaked loot table balance

<hr>

## <span class="yellow">[1.0.3] - 2023-04-29</span>
### Initial Release
- Over 55 upgradable spells
- Over 20 equipment items
- Weapon Imbuement System
- Armor Upgrade System
- 10 wizard armor sets
- 5 randomly generated structures
- 5 new enemies; a new boss
- And much more!



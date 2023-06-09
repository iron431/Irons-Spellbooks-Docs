---
layout: post
icon: fa-solid fa-list-ul
order: 9
toc: true
---
<style>
.yellow {
color:rgba(255, 194, 41, 0.5);
}
</style>
<hr>

## <span class="yellow">[1.1.4] (1.19.2 | 1.18.2) 2023-05-31</span>
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



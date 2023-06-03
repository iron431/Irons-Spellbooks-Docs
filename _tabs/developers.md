---
layout: post
icon: fas fa-code
order: 7
toc: true
---

## General
We don't currenly have an API to compile against so you need to link to the main mod jar. This is something on the roadmap. If you are interested in developing using us as a dependency you can help shape the roadmap by joining our discord and asking questions or providing feedback/suggestions.   

<a href="https://discord.gg/TRzEdrndM2"><img src="https://img.shields.io/discord/1104430139275743293.svg?label=&amp;logo=discord&amp;logoColor=ffffff&amp;color=7389D8&amp;labelColor=6A7EC2&amp;style=for-the-badge" alt="" width="129" height="28" /></a>

## Project Setup Using Gradle
### gradle.properties

These values should get set in your projects gradle.properties file.  It includes the versions for all Iron's Spells and its required dependencies

```kotlin
minecraft_version=1.19.2
forge_version=43.2.3

# Iron's Spells N SpellBooks
irons_spells_version=1.1.3

# Iron's Mod Dependencies
jei_version=11.6.0.1013
curios_version=1.19.2-5.1.3.0
tetra_version=289712:4414851
mutil_version=5.1.0
player_animator_version=1.0.2
caelus_version=3.0.0.6
geckolib_version=1.19:3.1.39

#General
gson_version=2.10.1
```

### build.gradle

In your repositories block you need to add the maven entries for Iron's and its required dependencies.

```kotlin
repositories {
  maven {
    name = "Iron's Maven"
    url = "https://code.redspace.io/releases"
  }

  maven { url = "https://maven.enginehub.org/repo/" }
  maven { url = "https://dl.cloudsmith.io/public/geckolib3/geckolib/maven/" }
  maven { url = "https://maven.theillusivec4.top" }
  maven { url = "https://cursemaven.com" }
  maven { url = "https://maven.blamejared.com" }
  maven { url = "https://maven.kosmx.dev/" }
}

```

You also need to add the following items to your dependencies block
```kotlin
dependencies {
    minecraft "net.minecraftforge:forge:${minecraft_version}-${forge_version}"
    implementation "io.redspace.ironsspellbooks:irons_spellbooks:${minecraft_version}-${irons_spells_version}"

    // GECKOLIB ***************************************************************************************************
    implementation fg.deobf("software.bernie.geckolib:geckolib-forge-${geckolib_version}")

    // CAELUS *****************************************************************************************************
    compileOnly fg.deobf("top.theillusivec4.caelus:caelus-forge:${minecraft_version}-${caelus_version}:api")
    runtimeOnly fg.deobf("top.theillusivec4.caelus:caelus-forge:${minecraft_version}-${caelus_version}")

    // PLAYER ANIMATOR ********************************************************************************************
    implementation fg.deobf("dev.kosmx.player-anim:player-animation-lib-forge:${player_animator_version}")

    // TETRA ******************************************************************************************************
    implementation fg.deobf("se.mickelus.mutil:mutil:${minecraft_version}-${mutil_version}")
    implementation fg.deobf("curse.maven:tetra-${tetra_version}")
    // If you want to run without tetra in dev comment the above 2 lines and uncomment the following line
    // compileOnly fg.deobf("curse.maven:tetra-${tetra_version}")

    // JEI ********************************************************************************************************
    compileOnly fg.deobf("mezz.jei:jei-${minecraft_version}-common-api:${jei_version}")
    compileOnly fg.deobf("mezz.jei:jei-${minecraft_version}-forge-api:${jei_version}")
    runtimeOnly fg.deobf("mezz.jei:jei-${minecraft_version}-forge:${jei_version}")

    // CURIOS *****************************************************************************************************
    compileOnly fg.deobf("top.theillusivec4.curios:curios-forge:${curios_version}:api")
    runtimeOnly fg.deobf("top.theillusivec4.curios:curios-forge:${curios_version}")

    // JSON *******************************************************************************************************
    implementation "com.google.code.gson:gson:${gson_version}"
}
```

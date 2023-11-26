---
layout: post
icon: fas fa-code
order: 10
toc: true
---

## General
With the 2.0.0 release of Iron's Spells N Spellbooks you can now register your own **_spells_** and **_schools_**!  There is also an API to compile against. If you are interested in developing using us as a dependency you can help shape the roadmap by joining our discord and asking questions or providing feedback/suggestions.   

<a href="https://discord.gg/TRzEdrndM2"><img src="https://img.shields.io/discord/1104430139275743293.svg?label=&amp;logo=discord&amp;logoColor=ffffff&amp;color=7389D8&amp;labelColor=6A7EC2&amp;style=for-the-badge" alt="" width="129" height="28" /></a>

## Example Repo
Here is an example mod that shows you how to register a spell and get started.

[https://github.com/iron431/Irons-Example-Mod](https://github.com/iron431/Irons-Example-Mod)

The example mod is setup to use our SNAPSHOT builds.
[https://code.redspace.io/#/snapshots/io/redspace/ironsspellbooks/irons_spellbooks](https://code.redspace.io/#/snapshots/io/redspace/ironsspellbooks/irons_spellbooks)

## Spell Registration
To register spells you will need to create your own registry using a DeferredRegister

```java
public class ExampleSpellRegistry {
    public static final DeferredRegister<AbstractSpell> SPELLS = DeferredRegister.create(SpellRegistry.SPELL_REGISTRY_KEY, IronsExampleMod.MODID);

    public static void register(IEventBus eventBus) {
        SPELLS.register(eventBus);
    }

    public static RegistryObject<AbstractSpell> registerSpell(AbstractSpell spell) {
        return SPELLS.register(spell.getSpellName(), () -> spell);
    }

    public static final RegistryObject<AbstractSpell> SUPER_HEAL_SPELL = registerSpell(new SuperHealSpell());
}
```

## Other Links

You can now create spells the same way we do in the core mod.  For examples of spells you can look at any of the spells here.

[https://github.com/iron431/Irons-Spells-n-Spellbooks/tree/1.19.2/src/main/java/io/redspace/ironsspellbooks/spells](https://github.com/iron431/Irons-Spells-n-Spellbooks/tree/1.19.2/src/main/java/io/redspace/ironsspellbooks/spells)

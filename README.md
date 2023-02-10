# iCS
### An interactive Character Sheet with a custom open ended "Unlicense"
---


&nbsp;&nbsp;&nbsp; The interactive Character Sheet was first built up by 3Douglas 3D Pihl. Because of the Open Gaming License (pre OGL 2) was looking at being changed by Hasbro via Wizards of the Coast. Because of the hurt this would cause many people to very quickly change & adapt to unforturnate events by these conglomerates. Out of that madness, 3D began showing an online usable Character Sheet. With a non-static character sheet not reliant upon OGL licensing this could help people continue to enjoy their favorite table top, RPG or larping online without worry.


&nbsp;&nbsp;&nbsp; iCS takes cares of many actions for the users and considerations in a manner that is based on a custom RPG layout concept. The internal algos help make the process of keeping up with a character sheet easy for all user levels. The algorithms used are as follows:

## Input Maker: This algorithm inserts an input with some customized information per area

## Weight: This algorithm considers the estimated weight of items based on their item type. When a player becomes over-burdened, an orange OB will appear next to the Armor words.
</br>
--
## Holding: This algorithm looks at how many items are being held when equiping and unequiping weapons and books.
 ### IF: A player that has strength that's higher then their strength combined with their phyiscal dexterity divided by their mental dexterity adjust up by 45 points can hold 2-handed items simultaneously.   
   "((S+PDex)/(Mdex))+45 <= strength" === Duel Wielding 2H Weapons
 
 ### THEN: If your character meets this criteria, equip a single handed object then equip a 2-handed weapon. Once equpied, unequip the 1-handed object then equip a second 2-handed weapon.  
   1H -> Hold Check (duel opened) -> 2H -> unequip 1H -> equip 2H (check not needed)
--

---
## User Details: This algorithm is a set of algorithms that keep track of various user character data.
 ### Armor Points: Points that represents the character's armor.
 Defense Points: Points that represents the character's attack power.
 Health Points: The number of points the user can take before dieing.
 Experience Points: The amount of total and active user experience points. 
 Inspirations: Revalations by the character based on a random roll & other factors.
---

Current Level: The character's level.

Character Speed: How fast is the character.

Moving Distance: How far can a character move (in meters).

Character Wealth: The amount of wealth the character has obtained including gold, metal coins & cryptocurrency Unsued Transaction Output Hashes.

Character Buy-In: The amount of cost to start a character for their attributes.

Attributes & Skill Boost: The value of the attributes and the skill boost paramaters.

Attribute Modifiers: Attributes Modifiers based on a unique cut-average.

Spell Level: The level of a learned spell.

Pages: Both a writable section of a paper object and the number of pages an object may contain.

Item Hashing: The current item's state as a reversable hash.

Item Rebuilding: The return API that tells how to rebuild the item via the hash.


<hr>

### Unique Actions with iCS

##Contracting (Bountys & Writing)

       Writing a contract for a bounty can allow you to hire for these actions. The Contracts also handle the writing actions for making journal entries and deeds for items/property/objects.

All bounties are based on on-game trust but do not turst the bounty writer for anything is possible.

Objects writen in your writables are not being seen by others.

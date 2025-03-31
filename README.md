# iCS
### An interactive Character Sheet Intelligently Acting with a custom open ended "Unlicense" to be used as a FOSS & Open Table-Top System
---
##### &nbsp;&nbsp;&nbsp; iCS is slowly becoming an "Intelligent Character Sheet" since the iCS system is doing some algo work and word recgonition. I don't think iCS [interactive] will reach ICS [Intelligent] standards very quickly but maybe one day iCS (interactive Character Sheet) will also be an ICS (Intelligent Character Sheet).

--
---
### To play with iCS live, visit https://3dd.in/iCS or to use the IFPS, try snagging the CID directly #QmNVmZ5LmRHnypPw8QDJYATGj6wxaRSspTQYYo1LS2SC5U to view, use & host locally!


### You can now download the most recent version release through Github! 
##### Look in the side panel or within the "Releases" section
---
--



## About iCS::


&nbsp;&nbsp;&nbsp; The interactive Character Sheet was first built up by 3Douglas "<i>3D</i>" Pihl to transfer generic character data from one game to another. When the Open Gaming License (pre OGL 2) was looking at being changed by Hasbro via Wizards of the Coast. Because of the hurt their changes would cause, many people (VTT and Table Top Players) very quickly began changing to adapt to the unforturnate events by these conglomerates. Out of that madness, 3D began working on making his Character Sheet usable online. With a non-static character sheet not reliant upon the OGL licensing (or any other pre-designed similar system), this could help people continue to enjoy their favorite table top, RPG or larping online without worry. Using Itty-Bitty v1 to create personalized iCS saves that allows for people to send, trade or continue previous saves. Wave Data APIs are used for sending objects into and out-of the interactive Character Sheet (iCS).

&nbsp;&nbsp;&nbsp; iCS takes cares of many actions for the users and considerations in a manner that is based on a custom RPG layout concept. Where OGL DnD may be mostly based upon common logic consideration & Pathfinder could be considered more Mathematical logical considersations, while both are relaint on rolls for checks. iCS uses a combination of both common logic & mathematical logical considerations & uses equational checks & rolls for randomizing possibilities. The internal algos help make the process of keeping up with a character sheet easy for all user levels, from handling equip allowances to determining if you are overburden. Almost every aspect that isn't strictly player choice, has been reduced to alorithms & equations. The algorithms used are as follows:

## Input Maker: This algorithm inserts an input with some customized information per area called for an input. This allows for anything that can be changed just needs the user to click on the section to be able to change it.

## Weight: This algorithm considers the estimated weight of items based on their item type. When a player becomes over-burdened, an orange OB will appear next to the Armor words. If a player is too underweight (overweight will be coming with this feature soon), they can becomed overburdened easier or even be unable to sustain their own weight (with armor, weapons, etc) which can cause loss of carry capability as well as loss of health points.

## Backfill1: This will return data from instered inputs back to where they were but with the inputted data as new information.


---
## Holding: This algorithm looks at how many items are being held when equiping and unequiping holdables (like weapons and books).
### &nbsp; IF: A player that has strength that's higher then their strength combined with their phyiscal dexterity divided by their mental dexterity adjust up by 45 points can hold 2-handed items simultaneously.   
#### &nbsp; &nbsp; &nbsp; "((S+PDex)/(Mdex))+45 <= strength" === Duel Wielding 2H Weapons
 
### &nbsp; THEN: If your character meets this criteria, equip a single handed object then equip a 2-handed weapon.
#### &nbsp; &nbsp; Once equpied, unequip the 1-handed object then equip a second 2-handed weapon.  
#### &nbsp; &nbsp; &nbsp; 1H -> Hold Check (duel opened) -> 2H -> unequip 1H -> equip 2H (check not needed)
---

---
## User Details: This algorithm is a set of algorithms that keep track of various user character data.
 ### &nbsp; &nbsp; Armor Points: Points that represents the character's armor.
 ### &nbsp; &nbsp; Defense Points: Points that represents the character's attack power.
 ### &nbsp; &nbsp; Health Points: The number of points the user can take before dieing.
 ### &nbsp; &nbsp; Experience Points: The amount of total and active user experience points. 
 ### &nbsp; &nbsp; Inspirations: Revalations by the character based on a random roll & other factors.
 ### &nbsp; &nbsp; Player Weight: Tracks player weight <code>[lbs.oz]</code>.
 ### &nbsp; &nbsp; Player Height: Tracks player height <code>[feet.inches]</code>.
 ### &nbsp; &nbsp; Player Ratio: Tracks players weight:height ratio. 
 #### &nbsp; &nbsp; &nbsp; "((Weight)/(Height))-21" = Player Ratio.
 ### &nbsp; &nbsp; Player Age: Tracks players age.
 ### &nbsp; &nbsp; Player GPA|IQ: Tracks Player GPA & IQ. Determines one's GPA if an IQ is given & determines one's IQ if a GPA is given.
 #### &nbsp; &nbsp; &nbsp; "((0.004)/(IQ))-1" = Player GPA.
 #### &nbsp; &nbsp; &nbsp; "(((GPA)/2)*0.333)*100" = Player IQ.
 ### &nbsp; &nbsp; Player Hometwon: Tracks players hometown. Has a list of recgonizable village names, town names, city names & metropolis names.
 ### &nbsp; &nbsp; Player Population: Tracks players hometown population.
 ### &nbsp; &nbsp; Player Favs: Tracks players favorites (up to 3 different favorites).
 ### &nbsp; &nbsp; Player Belief: Tracks players Belief.
 ### &nbsp; &nbsp; Player Alignment: Tracks players alignment.
 ### &nbsp; &nbsp; Player Background: Tracks players background.
 ### &nbsp; &nbsp; Player Skill Boosted: Tracks players amount that their skills are boosted by.
 ### &nbsp; &nbsp; Player style: Tracks players style.
---

## Current Level: The character's level.

## Character Speed: How fast is the character.

## Moving Distance: How far can a character move (in meters).

## Character Wealth: The amount of wealth the character has obtained including gold, metal coins & cryptocurrency Unsued Transaction Output Hashes.

## Character Buy-In: The amount of cost to start a character for their attributes.

## Attributes & Skill Boost: The value of the attributes and the skill boost paramaters.

## Attribute Modifiers: Attributes Modifiers based on a unique cut-average.

## Spell Level: The level of a learned spell.

## Pages: Both a writable section of a paper object and the number of pages an object may contain.

## Item Hashing: The current item's state as a reversable hash.

## Item Rebuilding: The return API that tells iCS how to rebuild an item via its hash.
---


# Unique Actions with iCS

## Contracting (Bountys & Writing)

### &nbsp; Writing a contract for a bounty can allow you to hire for these actions. The Contracts also handle the writing actions for making journal entries and deeds for items/property/objects.

#### &nbsp; &nbsp; All bounties are based on on-game trust but do not turst the bounty writer for anything is possible.

#### &nbsp; &nbsp; Objects writen in your writables are not being seen by others until you share them.
   
#### &nbsp; &nbsp; Importing Items

### &nbsp; If you have an item hash from another player or round, you can import the item as old-new. This can allow you to transfer items across games with just a hash or save usable game items for a list or database for all players to have all the same item data.

#### &nbsp; &nbsp; This can also allow for users to transfer messages or contracts for a new layer of player actions.

### &nbsp; Pressing the "s" button below each item will give the current status of that item as a hash. This hash can be shared and anyone with that hash can import that item. This is for side-layer player actions, player contracts, debts, onlline table-top gaming & Virtual Table-Tops (VTT).

### &nbsp; To import an item from an item hash, click "Add Item" then insert, "print" into the first input field and then insert, "import" or another import type action command to activate the importing input. Place the item hash in that blank input and click, "Add" to add that item.

### &nbsp; &nbsp; &nbsp; If an item's code is malformed from transferring, recieving users may have to click a final item type button.
---

---
## Import:

#### &nbsp; &nbsp; &nbsp; Add Item --> "drive" --> "import" --> item importer

### &nbsp; :To Access:   
### &nbsp; &nbsp; :Item Importer:
### &nbsp; &nbsp; Input 1 --> "Drive"
### &nbsp; &nbsp; Input 2 --> "import"
### &nbsp; &nbsp; What you get --> Item Importer App

## &nbsp; !**!Do Not Import Funds This Way!**!
---

---
## Books (Reading VS Holding)

   Some books are held to gain acces to item's attribute de/booster. While other books are a one time reading action. Scrolls, pages, books and similar may be considered "readables" which are all conted as 'books'.

### &nbsp; &nbsp; Hoover to learn more about most actions.
---

---
## Exchaning & Sending

### &nbsp; &nbsp; Anyone can send crypto or fiat that is in their account and the options they offer. Using the banking exchange will let you experience the crypto/fiat market from buying and selling cryptocurrency. The banking application can imprint your personal market data onto your items. Tranferring an item with market data will effect the market of the players that import that item.

### &nbsp; &nbsp; Click "Add Item", type "inet" then click the "change" button. Now type in "forex" or "exchange" then click "set" button to open the banking and trading market page. The trading market page will let you trade your currencies as well as send fiat item hashes or accept fiat item hashes from other players.
To Access Banking Application:
 
#### &nbsp; &nbsp; &nbsp; Add Item --> "online" --> "bank" --> Exchange & Bank Transfers


### &nbsp; &nbsp; Click "Add Item", type "inet" then click "change". Now type in "transact" or "send" then click "set" button to open the cryptocurrency wallet page. The cryptocurrency wallet page will let you send your cryptocurrencies as Unspent Transaction Hashes (UTXO Hash). Copy and send the hash once finailzed.
To Access Wallet:
  
#### &nbsp; &nbsp; &nbsp; Add Item --> "online" --> "send" --> Wallet


### &nbsp; &nbsp; Click "Add Item", type "inet" then click "change". Now type in "coin" or "send" then click "set" button to open the cryptocurrency wallet page. The cryptocurrency wallet page will let you send your cryptocurrencies as Unspent Transaction Hashes (UTXO Hash). Copy and send the hash once finailzed.
 
### &nbsp; To Access Wallet:  
#### &nbsp; &nbsp; &nbsp; Add Item --> "online" --> "bank" --> Exchange & Bank Transfers


### &nbsp; &nbsp; Going through the same processs except typing in "coin" or "sweep" instead of "coin" or "send" will bring up the cryptocurrency sweeper to accept cryptocurrency UTXOs use the Wallet UI commands. To get the Crypto Sender to send cryptocurrency UTXOs use the Wallet UX commands.
 
### &nbsp; To Access Sweeping Application:
#### &nbsp; &nbsp; &nbsp; Add Item --> "online" --> "sweep" --> Sweeping UTXOs

### &nbsp; &nbsp; **Use the Recgonized List for more command options**

### &nbsp; :To Access: 
#### &nbsp; &nbsp; Accessing What -- 1st Input -- Item Type Input (2cd Input) -- To Do What
#### &nbsp; &nbsp; Banking App -- "Online" -- "Bank" -- Buy/Sell/Trade Fiat & Crypto
#### &nbsp; &nbsp; Send Crypto App -- "Online" -- "Send" -- Send Crypto (obtain a P2P UTXO Hash to send to recieving party)
#### &nbsp; &nbsp; Send Crypto App -- "Online" -- "Coin" -- Sweep UTXO Hashes to accept Crypto
---

---
## Commands

### &nbsp; &nbsp; Comands are put in the first two inputs after clicking to "Add Item". The first input commands are normally names of items. This section also does internal triggering but there's three other user commands possible, "data", "print" & "online". Data, Print & Online are unimportant commands (because there are different commands to do the same task as these) but are helpful for users remembering the options for the next set of commands.

### &nbsp; &nbsp; The second set of input commnads are normally item types but there are a handful of recognized commands that perform various actions like access the Banking app, the Crypto wallet & Cheats. In the list of recgonized inputs, unless they say "trigger" or are for "triggers" then they work on this line of commands. Going through that list will help you navigate around the iCS application.

#### &nbsp; &nbsp; &nsbp; Most commands will work under this process tree: command1, command2, command3*, command-expander*.

---
## Input Process Trees

### &nbsp; :Item:
##### &nbsp; &nbsp; &nbsp; Name -- Type* -- Details* -- Extras* -- Hash*

### &nbsp; &nbsp; :Data:
### &nbsp; &nbsp; "Data" -- Command -- Hash* -- De/Encoder

### &nbsp; :Internet:
### &nbsp; &nbsp; "Online" -- Command -- Hash* -- De/Encoder

#### &nbsp; &nbsp; * an astrik represents an injection possible point
#### &nbsp; &nbsp; &nbsp; " " words inside quotation marks are verbatim command input
---

---
## Unlocked License (UnLicense)

### &nbsp; &nbsp; The Unlocked License is a form of License that has only 2 stimpulations for validity, which are as follows:

#### &nbsp; &nbsp; 1) If previous credits are available & visiable without clicking anything or going anywhere.
#### &nbsp; &nbsp; 2) if this license is available & visiable with a maximum of a single click or without any clicking.

### &nbsp; &nbsp; The Unlocked License uses predetermined clauses to consider if the license and the use of the license is valid. To determine if this license is valid follow these stimpulations, which are as follows:
###### Credit to the previous workers, builders, originators and others involved with the web object/app/page/document and it's content before & of the current version of the web object/app/page/document & content must be visiable without any clicking, hiding behind any button, object, terms of service, conditions, terms, color-blending, background hiding, font color hiding or otherwise that is not directly viewable by users.
This license must be visiable with a maximum of a single click mechanic, a single linked page (must be a direct to page or direct to file link) or directly on the page to the users.

###### If this license is valid, then this web object/app/page/document & the use of this web object/app/page/document is allowed by this license. If this license is not valid, then the web object/app/page/document & use of this web object/app/page/document is not allowed. If the original credit & any additional credits are left in-tact and are visible as previously described in this license, then this license is valid. If this license is visible either through a single click mechanic, a single linked page (must be a direct to page or direct to file link) or directly on the page then this license is valid.

###### No user specific data is allowed to transfer to new users, owners, builders, creators or any other enitity, person, company, governemnt or electronic identity or intelligence. This license is over the usability and the web object/app/page/document itself not the user-specific data inputted, automated, generated or processed from use of the web object/app/page/document. The user that inputs data as well as causes the creation of data through automation, generation, APIs or processing is for that user alone. This does not mark owners of data inputted, automated, generated, pulled in, proccessed or considered but does deny the builders, creators, hosts, interactors of the web object/app/page/document allowance of being called owners of any data inputted, automated, generated, pulled in, proccessed or considered through this or any future version of this web object/app/page/document. This license cannot be revoked, removed, changed or withdrawn without causing the license for that specific version of the web object/app/page/document. To stop using this license for future versions of the connected web object/app/page/document, you will have to create a new version of this web object/app/page/document without this license but must include that the new version is not an Unlocked License Web Object in a clear, readable format that's directly viewable by users without any clicking or hiding of any kind.
---

---
## Recgonized Items List

### &nbsp; &nbsp; These are the offically recognized item types to increase capabilities of the interactive Character Sheet (iCS). Weapons will prompt the Power Level & Holding options. Arrows will push to the secondary weapon slot (only used for arrow type weapons/ammo). Armors will add wieght but will also prompt the Defense Level & Armor Form options. Wearables add weight of a constant 0.1 lbs per wearable but prompts the Level & Form options. Readables/Books add weight equivalent to the number of pages in the readable object but also prompts the Pages & Type options.

### &nbsp; &nbsp; Input one of these recgonized words as an item type to access the usability of that word type.


### &nbsp; &nbsp; Weapons:
###### weapon, sword, axe, hammer, bow, shield, broadsword, knife, nife, kife, butcher, blade, nail, scyth, sicle, sickle, sikle, fan, mace, dagger, long axe, 2-handed, shears, sai, javelin, trident, spear, spears, staff, stalves, bomb, granade, tonfa, nunchucks, lightsaber, lightsabor, caltdrops, pick, pickaxe, sling, blow gun, blowgun, darts, dart, sledgehammer, spade, gun, rifle, machinegun, machine gun, ammo, ammunition, ammu, whip, nine tails, 9-tails, 9tails, nine-tails, 9 tails, tail, surujin, stars, throwing, throw, throws, flail, net, spiked, spike, crossbow, crossbows, shells, cannon, balls, ball, weaponized pad, weaponized bracer, weaponized bracers, thorn, thorns, charkram, morning-star, morningstar, morning star, rapier, bastard, long-sward, longsword, lance, long-sword, short, short sword, shortsword, short-sword, sward, battleaxe, light crossbow, starknife, longspear, long spear, spiked chain, chain, ranseur, club, spiked club, boomerang, halbred, shotgun, nuke, nuclear arms, nuclear arm, blaster, pistol, blaster rifle, blaster pistol, darksaber, darksabor, lightsaber pike, pike, honor guard rifle, smoke bomb, somkebomb, flashbang, flame rifle, flamethrower, dual lightsaber, dual lightsabor, quad cannon, dual cannon, booma, missle launcher, MLRS, mlrs, usp, .45, magnum, .44, m9, desert eagle, pp2000, bbgun, bb, pp, g18, m93, raffica, tmp, machine pistol, spas, spas-12, spas12, aa-12, aa, 12, striker, ranger, sawedoff, sawed off, m1014, 1014, 1887, model 1887, at4, rpg, rpg7, rpg-7, m79, stinger, excalibur, cloud sword, pistol sword, bladed pistol, bayentte, bayonetta, talon, war-axe, eared, glavie, boar pike, boarpike, partizan, poke-axe, awi-pike, awi, awl, guisarme, bills, swiss bill, voulge, fork, manarifle, polearm, handaxe, rod, manapistolsaya, ninja-to, ninjato, katana, kuhai, shuriken, makibishi, shuko, plasma sword, plasmasword, plasma, ma4d, br55, ma7b, ma5c, ma5k, mr55-m45, m45, ma6c, ma5b, m8, smg, br55at, br55at-ww, br55cw-sa, m7, ma2b, ma4k, m6b, m6D, m6x, br55hg, saw, sawgun, shotty, br55dm-r, sniperifle, sniper rifle, sniperrifle, br55-ss, m90, mk1, mk 1, mk 2, mk2, ssm, cqc, m6j, m6c, m6e, cw, stanchion, m99 stanchion, aptr, ma4b-aptr, 1173, m90 1173, punisher, brute shot, beam rifle, carbine, h2, h1, fuel rod, fuel rod gun, needler, gravity hammer, fist of rukt, rukt, spiked bomb, plasma cannon, gravity gun, portalgun, portal gun, megaman, megagun, meagman gun, frizbar, gale, claw, double dragon, sucker punch, masamune, gladius, spatha, home-wrecker, homewecker, ture blade of the east, eastern blade, guan dao, naginata, kopis, famboyant, pattah, ajanta, barabudur, konarak, katti, natar temple sword, ram dao, ram horn, kukri, kora, kukri, hostala, ellora, katar, wrist blade, hatchet hands, hatchet, cestus, claws, blade talons, blade talon, hatchet hand, wrist blades, scissors, scissors katar, quhab, fascia, hand scythe, scythe, swayyah, war fist, natalya mark, Natalya's mark, natalyas mark, uzi, urumi, vadi, otta, colt, beretta, 9mm, 22, long rifle, sub-machine, submachine, sub machine gun, sub-machine gun, submachine gun, assult rifle, ar15, ar16, ar18, m1, granade launcher, moltav, tekko, stiletto, wand, wands, limb, arm, leg, pipe, monkeywrench, pipewrench, metal, strut, arm, prostetic, prosthetic, mechanical, biological, extension, limb



### &nbsp; &nbsp; Bow & Crossbow ammo:
###### arrow, arrows, twig, stick, bolt, bolts



### &nbsp; &nbsp; Armors:
###### tunic, armor, glove, helmet, helm, hat, hood, chest plate, chestplate, breast plate, breastplate, guard, shoe, garb, shoes, boots, sneakers, runners, streamers, gloves, comb, visor, gorget, pauldron, counter, rerebrace, brace, plackart, fauld, tasset, tassle, tassel, cuisse, gauntlet, gauntlets, fan-plate, fan plate, fanplate, greave, greeve, sabaton, stop rib, stoprib, rib, gardbrace, vambrace, fauld, mail, chainmail, platemail, cloth, leather, kabuto, nodowa, sode, sendan-no-ita, sendan no ita, sendannoita, kote, kasazuri, haidate, sune-ate, sune ate, suneate, kyahan, isurumaki, do, shoulder armor, soulderarmor, hand guard, tekko, hakama, pants, thigh guard, thighguard, tassets, tasset, tabi, socks, hitatare, robe, shirt, nape guard, napeguard, shikoro, helmet crest, hemlmetcrest, maedate, watagami, shoulder strap, shoulderstrap, strap, bascinet, vervelles, aventail, spaulder, haubergeon, lames, demi, denim, wing, gatlings, wrist gauntlets, wristgauntlets, wrist bracers, bracer, crotch plate, thigh guanlets, knee pads, kneepads, utility belt, belt, suspenders, torso guard, torso plate, torso pad, arming cap, armingcap, cap, doublet, chain maille, chainmaille, chainmalle, chain malle, hose, pantyhose, lingera, lungera, crowl, salade, salet, schalern, bevor, beavor, placard, tuille, buckle, belt buckle, skull, sight, besagne, kettle helm, fur, cape, bag, pouch, focus, sandles, sandels, tubesocks, knee high, stiletos, stileto, curb stompers, curbstompers, kleats, kleets, kelt, sporran, sgain, flashers, brogues, ghillie, argyll, leather hat, leather cap, leatehr jacket, leather armor, leather pants, leather shoes, jacket, pin, scarf, straps, cloak, hooded cloak, sock, sandel, shroud, moccasins, jynco, mjolnir, powered assult armor, powered armor, beanie, Link's Hat, Links Hat, Link Hat, Mark V, Master Chiefs, Mark VI, tshirt, t-shirt, v-neck, vneck, turtleneck, seater, parka, wind breaker



### &nbsp; &nbsp; Wearables:
###### jewerly, ring, necklace, earrings, hoops, hoop, piercing, piercings, rings, necklaces, earring, ear hoop, ear ring, earhoop, earloop, ear loop, ear chain, earchain, neckchain, neck chain, pendant necklace, arm bands, wrist bands, bangels, bangel, bangle, collar, chocker, princess, matinee, opera, lariat, rope necklace, neck rope, neckrope, channel, bezel, pave, three-stone, -stone, inspired, prong, halo, split shank, splitshank, solitaire, industrial, forward helix, helix, flat, curved barbell, anti helix, anti-helix, antihelix, snug, targus, dermial, micro-dermial, microdermial, upper lobe, lobe, bridge, third eye, nasallang, austin bar, septril, septum, rhino, medussa, medusa, sports ring, champion ring, captive bead ring, navel, navel ring, choker



### &nbsp; &nbsp; Elements:
###### fire, cold, ice, wind, sun, dark, rosen, natrual, enfluenced, high, techy, fearfull, feared, fearless, hyped, electric, earthed



### &nbsp; &nbsp; Element Title Triggers:
###### Dragonbreath, Icebreath, fogbreath, fire, flame, flarred, fanned, chared, char, campfire, torch, torched, flamed, dragon breath, scorched, chorched, charcoal, on fire, flaming, hot, heat, cold, snow, snowing, frostbite, frost, frosted, frosting, frothed, frothy, chilled, chilly, frosty, blue snake bite, tundra, hypothermia,crisp, sharp, edged, leveled, ready, blizzard, ice, frozen, freezer burn, ice burn, cold burn, airy, airey, aireay, aired, airee, wind, gusts, huricane, hurican, tornado, sunny, spring, bright, sunny, sun, flared, sunrays, sun rays, rays, light, dreary, deary, gloomy, goth, gothic, punk rock, metal, death, dark, night, moon, starie, stary, staree, reflect, portal, multiverse, multplex, multi-universe, metaverse, metaversal, universal, nebula, cloud, cloudy, complex, rose, strong, natrual, stone, granite, onxy, crystal, crystaline, prisym, prisim, prysim, rainbow, skidish, stitich, sketch, stetch, wretch, wicked, green, 420, smoke, toke, bruh, brosiv, herb, marijuana, smoked, joint, blunt, stash, technical, electrician, technician, mechanical, geared, engerniered, engerneer, engineer, engineered, engineering, unsure, unaware, unspoken, hesited, scared, shocked, possesed, haunted, horror, horrific, scary, feared, spook show, manslaughter, holy, higher, power, above, regard, missle, marine, god-like, god like, demigod, demegod, god son, god daughter, soul, reaper, heaven, angel, god, jesus, marry, susan, geroff, gregory, leslie, belief, gods, spark, sparky, sparked, shocked, elctro, electric, galantic, galaxian, galatical, volts, amps, spider, grounded, land, solid, landed, landing, low



### &nbsp; &nbsp; Readables
###### page, tomb, scroll, spellbook, spell book, book, bible, quran, bhagavad Gita, bhagavad, composition, torah, spiral, notebook, diary, scripture, vedas, upanishads, upanishad, brahmana, aranyaka, dhanurveda, ayurveda, upa-vedas, upa-veda, veda, sruti, smriti, ithihasa, mahabharata, ramayana, purana, agama, darshana, mahapurana, mahapurava, upa, upa puranad, puranad, puranas, purana, vasihnava, shaiva, saktha, nyaya, vaisheshika, sankhya, yoga, mimamsa, uttara, pentateuch, genesis, exodus, leviticus, deuteronomy, psalms, proverb, proverbs, ecclesiastes, sirach, vajur, sama, kojiki, adi, granth, orthodox, book of mormon, necronomacon, perbindeshi, lolita, decameron, droll, cookbook, handbook, letter, works, works of, mein kampf, rangila rasul, stanic verses, satanic bible, lajja, zhuan falun, papers, paper, death note, deathnote, zhou enlai, mao, bloody myth, capital and ideology, of life, les moeurs, Les MÅ“urs, suicide note, suicidenote, ivanhoe, oliver twist, manifesto, the jungle, of erotic, world of , die gesteinigten, question of guilt, lysistrata, El SeÃ±or Presidente, el senor presidente, hind swaraj, jugbani, durdiner, zatri, bisher bashi, vangar gaan, chandrabindu, islam through hadis, annexation of sikkim, soft target, furqan, shivaji, jinnah, great soul, bulpington, of blup, brave new world, of good will, the martyr, laws of life, the constitution, constitution, bill of, bill of rights, honourable estate, dutch interior, borstal boy, little black sambo, sambo, little black book, black book, green book, white book, red book, yellow book, book, sophies choice, Sophie's Choice, schindlers ark, Schindler's Ark, da vinci code, programming, language, code, code, codex, grover, of light, fity shade, of sanity, rebirth:, rebirth, rebirth , gay is, peichi, à®ªà¯‡à®¯à¯à®šà¯à®šà®¿, notre ami le roi, le roi predateur, le roi, the rape of sita, of sita, cover-up general, coverup genera, cover up general, inter the river, great replacement, my watch, fra kristiania-bohemen, fra kristiania, albertine, snorri the seal, of the red ruby, satyarth prakash, satyarth, prakash, jinnah of, about muhammad, noli me tangere, untold story, political dos, document, documents, may handlang ang umaga, kalatas, labas, mirror of the polish crown, historia do mundo para as criancas, mundo para as, the boys, man who wouldn't stand up, man who wouldnt stand up, love comes later, thalia, new world translation, king james, version, rights of man, looing backward, elders of zion, protocols, protocol, animal farm, 1984, ninteen eighty-four, ninteen eighty four, nineteen eightyfour, doctor zhivago, one day in , the life of, first circle, the circle, gulag archipelago, apocalypse, queen of sheba, goat days, frzai-e-amaal, frzai e amaal, value, price and profit, profit, and state, & state, of surplus value, anarchism or socialism, marxism, marxist, marx, heroines, and revolution, & revolution, time, foward, of the USSR, is all about, wisdom of jihad, wisdom of, that nullify, red lines, frankenstein, world of, of africa, soul on ice, is my life, burger's daughter, burgers daugher, julys people, jul's people, year 501, bad samaritans, samaritan, samaritans, one spoon on this earth, ulysses, devil's discus, devil discus, devil bible, devil's bible, king never smiles, areopagitica, rights of man, lord horror, anarchist cookbook, kill or get killed, canterbuy tales, tales, meritorious price of our redemption, moll flanders, fanny hill, candide, uncle tom's cabin, uncle toms cabin, elmer gantry, tropic of cancer, forever amber, grapes of wrath, howl, pedagogy of the oppressed, federal mafia, 60 years later, operation dark heart, paradise of the blind, nickel-plated-feet gang, les pieds, dans le maquis, new class, curved river, on fierce wound, thoughts of a corpse, storytellers, of the wind, deuterocanon, epistles, canon law, common law, law, protestant bible, apocrypha, manasseh, chronicles, maccabees, enoch, titus flavius, wycliffe, hussite, reformation, deuterocanonical, luther bible, lutheran bible, lutheran, tyndale, of jonah, geneva bible, coverdale, dutch bible, casiodoro de reina, bear bible, biblia del oso, alfonsia, cipriano de valera, valera, pocket bible, pocket book, jewish hebrew bible, protocanon, protocanonical, interestamental, robit, ecclesiasticus, baruch, susanna, bel and the dragon, lined paper, rag paper, handbill, tag, poster, bound words, bound texts, sea scrolls, dead sea scroll, sea scroll, words, scribing, scribings, spell, spell book, spell page, spell scroll, sealed, opened, manual



### &nbsp; &nbsp; Writables
###### spiral, papers, paper, deed, bounty, journal, blank, blank book, unsealed, notebook



### &nbsp; &nbsp; Hometowns
##### Villages: 
###### Kochan, Ablanista, Koprivlen, Laki, Nova Lovcha, nova Leski, Paril, Petrelik, Babyak, Floating Villages, Bibury, Ait-Ben-Haddou, Hallstatt, Juzcar, Eze, Inle Lake, Lamayuru, Isla Del Sol, Del Sol, Larung Gar, Larung, Marsaxlokk, Oia, Navala, Navala Village, Floating, Floating Village, Enkeri, Enkeri Village, Nubian, Bubia, Nubia, Nubian Village, Nuuk, Pariangan, Palangan, Punji, Pygmy, Batwa, Pygmy Batwa, Pygmy Village, Batwa Village, Shirakawa, Xidi, Swat Valley, Wenen, Jukkasjarvi, Kash Goz, Kash, Goz, Giethoorn, Gasadalur, Freundenberg, Zell am See, Wagrain, Sauris-Zahre, Isola del Giglio, Castelo Novo, Castelo, Novo, Rasinari, Bohinj, Rupit, Murten, Andermatt, Birgi, Thai Hai, Guadalupe, Old Town, Choke Mountains Ecovillage, Aguarico, Angochagua, Mestia, Kfar Kama, Umm Qais, Creel, El Fuerte, Ksar Elkhorbat, Moulay Bouzerktoune, Lamas, Raqchi, Pyeongsa-ri, Pyeongsa


##### Towns: 
###### Smalltown, Albarracin, Ban Rak, Ban Rak Thai, Rak Thai, Banos, Bar Harbor, Biei, Bled, Bocas del Toro, Bocas, del Toro, Carmel-by-the-Sea, Colonia del Sacramento, del Sacramento, Colonia, Castle Combe, CastleCombe, Combe, Esperance, Gokayama, Gordes, Goreme, Guatape, Hatta, Ilulissat, Iruya, Itchan Kala, Kaikoura, Kalk Bay, Kralendijk, Lamu, Lauterbrunnen, Luang Prabang, Luang, Prabang, LuangPrabang, Luderitz, Lunenburg, Mandawa, Moulay, Idriss, Moulay Idriss Zerhoun, Zerhoun, Navala, Niagra-on-the-Lake, Paraty, Penglipuran, Port Fairy, Praiano, Raquira, Rothenburg ob der Tauber, ob der Tauber, Tauber, Sai Kung, Sapa, Sayulita, Sedona, Sidi Bou Said, Sidi, Bou, Bou Said, Sitka, Siwa, St Augustine, Augustine, St. Augustine, Saint Augustine, Tepoztlan, Vinales, Zhouzhuang, Wallace, Marfa, Jim Thorpe, Bisbee, Eureka Springs, Yellow Springs, Helen, Whitefish, Taos, Mount Dora, MountDora, Astoria, Lanesboro, Hillsboro, Galena, New Harmony, Salina, Lindsburg, Joseph, Lititz, Beaufort, Port Townsend, Townsend, Ferndale, Breaux Bridge, Eclectic, Delight, Why, Unalaska, Rough and Randy, Rough & Randy, Mystic, Superior, Slaughter Beach, Enigma, Sandwich, Electric City, Cal-Nev-Ari, Tightsqueeze, Tuxedo, Loveladies, Truth or Consequences, What Cheer, Bald Head, Halfway, Hometown, West Virigina, Hometown,West Virigina, Satan's Kingdom, Satan's Kingdom, Satans Kingdom, North Star, Hot Coffee, Monkey's Eyebrow, Monkey's Eyebrow, Monkeys Eyebrow, Monkies Eyebrow, Intercourse, Waterproof, Tiki Island, Valentine, Sweet Lips, Elmo, Wineglass, Miner's Delight, Miner's Delight, Miners Delight, Normal, Santa Claus, Defiance, Dead Women Crossing, Sublimity, Yeehaw Junction, Bread Loaf, BreadLoaf, Kismet, Ketchuptown, Love Valley, Luck, Humansville, Porchupine, Killdeer, Volcano Village, Good Grief, Woonsocket, Upton Snodsbury, Pucklechurch, Barton in the Beans, Curry Mallet, Droop, Throop, Plumpton, Lickfold, Warninglid, Nomansland, Uploders, Matching Tye, MatchingTye, Nether Wallop, NetherWallop, Poling, Patching, Climping, Didling, Crudwell, Puddletown, Tolpuddle, Affpuddle, Braintpuddle, Westward Ho!, WestwardHo!, Westward Ho, WestwardHo, Upper Bucklebury, UpperBucklebury, Mudford Sock, MudfordSock, New Invention, NewInvention, picklescott, Marsh Gibbon, MarshGibbon, Blubberhouses, Mamble, Tedstone Wafre, TedstoneWafre, Hose, Hoby, Shoby, Thumpton, Bitchfield, Over Peover, OverPeover, Wetwood, Wetwang, Papplewick, Bishop's Ichington, Bishop's Ichington, Bishops Ichington, Bishop'sIchington, Bishop'sIchington, BishopsIchington, Queen Camel, QueenCamel, Great Snoring, GreatSnoring, Cement, Laramie, Larrimah, Bidgeegud, Derby, Lawton, Alesund, Bruges


##### Cities: 
###### Abidjan, Accra, Adana, Addis Ababa, Adelaide, Agre, Ahmadabad, Aleppo, Aleppohalab, Aleepo Halab, Alexandria, Algiers, Allahabad, Almaty, amman, Amristar, Ankara, Anshan, Baghdad, Baku, Bandung, Bangalore, Bangkok, Baotou, Barcelona, Barquisimeto, Barranquilla, Basrah, Beijing, Beirut, Belem, Belgrade, Belo Horizonte, BeloHorizonte, Benghazi, Benin, Berlin, Bhopal, Birmingham, Bogo Ta, Bogota, BogoTa, Bogo, Brasilia, Brazzaville, Brisbane, Bucharest, Budapest, Buenos Aires, Bursa, Busan, Cairo, Cali, Campinas, Capetown, Caracas, Casablanca, Changchun, Changsha, Changzhou, Chelyabinsk, Chengdu, Chennai, Chicago, Chittagong, Chongquin, Ciudad Juarez, CiudadJuarez, Conakry, Copenhagen, Cordoba, Curitiba, Daegu, Daejon, Dakar, Dalian, Dallas, Damascus, Dar es Salaam, DarEsSalaam, DaresSalaam, Dar Es Salaam, Datong, Delhi, Dhaka, Dnipropetrovsk, Donetsk, Douala, Durban, Ecatepec, Ekaterinburg, Faislabad, Fortaleza, Foshan, Freetown, Fukoka, FreeTown, Fuzhou, Giza, Goiania, Gudalajara, Guangzhou, Guarulhos, Guatamala City, Guayaquil, Guiyang, Gujranwala, Gwangju, Wala Wala Washinton, WalaWala, Wala Wala, WalaWalaWashinton, Gwangju, Haiphong, Hamburg, Handan, Hangzhou, Hanoi, Haora, Harare, Harbin, Havana, Hefei, Hiroshima, Ho Chi Minh City, HoChiMinh, HoChiMinhCity, Ho Chi, Chi Minh, Ho Chi Minh, Minh City, HCMC, Hong Kong, Houston, Hyderabad, Ibadan, Incheon, Indore, Irbil, Isfahen, Istanbul, Izmir, Jaipur, Jakarta, Jeddah, Jilin, Jilan, Jodphur, Johannesburg, Kabul, Kaduna, Kano, Kanpur, Kaohsiung, Karachi, Kawasaki, Kazan, Kharkiv, Khartoum, Khulna, Kiev, Kinshasa, Kitakyushu, Kobe, Kolkata, Kowloon, Kuala Lumpur, KualaLumpur, Kunming, Kyoto, La Paz, LaPaz, Lapaz, Lagos, Lahore, Lanzhou, Lean, Lima, London, Los Angeles, Luanda, Lubumbashi, Lucknow, Ludhiana, Luoyang, Lusaka, Madrid, Maiduguri, Makassar, Managua, Manaus, Manila, Maputo, Maracaibo, Mashhad, Mecca, Medellin, Medina, Meerut, Melbourne, Mexicali, Mexico City, Milsan, Minsk, Mogadishu, Monterrey, Montevideo, Montreal, Moscow, Mosul, Multan, Mumbai, Mumbai Bombay, MumbaiBombay, Bombay, Munich, Nagoya, Nagpur, Nairobi, Nanchang, Nanjing, Nanning, Napoli, Nashik, New York City, New York, NYC, Big Apple, NewYork, NewYorkCity, NYCity, Nesahualcoyotl, Nizhny Novgorod, NizhnyNovgorod, Novosibisrk, Odessa, Omdurman, Omsk, Osaka, Palembang, Paris, Patna, Perm, Perth, Peshawar, Philadelphia, Phily, Philly, Phnom Penh, PhnomPenh, Phnompenh, Phnom, Penh, Phoneix, Phoenix, Pimpri Chinchwad, PimpriChinchwad, Pimpri, Chinchwad, Port Harcourt, Harcourt, PortHarcourt, Port-Au-Prince, Port Au Prince, Port Prince Gold, Prince Gold Port, Port Gold Prince, PortAuPrince, AuPrince, Au Prince, Porto Alegre, Portoalegre, PortoAlegre, Prague, Puebla, Pune, Pyongyang, Quingdao, Qiqihar, Quito, Rabat, Rajkot, Ranchi, Rawalpindi, Recife, Rawalpindi, Rio de Janerio, RiodeJanerio, RioDeJanerio, de Janerio, Rio, Janerio, Riyadah, Rome, Rosario, Rostov on Don, Rostov, on Don, Don Rostov, Salvador, Samara, San Antonio, Antonio, San Diego, DanDiego, Sanaa, Santa Cruz, SantaCruz, San Tiago, Santiago, Tiago, Cruz, Santo Domingo, Domingo, SantoDomingo, Sao Paulo, SaoPaulo, Paulo, Sapporo, Semarang, Sendai, Seongnam, Seoul, Shanghai, Shenyang, Shenzhen, Shiraz, Shiziahuang, Shubra El Khemia, Shubra, El Khemia, Khemia, ShubraElKhemia, ShubraKhemia, Shubra Khemia, Singapore, Sofia, Soweto, St Petersburg, St. Petersburg, StPetersburg, Saint Petersburg, SaintPetersburg, Stockholm, Surabaya, Surat, Suzhou, Sydney, Tabriz, Taichung, Taipei, Tai Pei, Taiyuan, Tangshan, Ta Shkent, TaShkent, Tashkent, Tbilisi, Tegucigalpa, Tehran, Tianjin, Tijana, Tokyo, Marijuana, Toronto, Tripoli, Tri Poli, TriPoly, Tripoly, Tshwane, Tshwana Pretoria, TshwanaPretoria, Pretoria, Petoria, Peteoria, Tunis, Ufa, Ulsan, Urumqi, Vadodara, Valencia, Varanasi, Vienna, Viena, Volgograd, Vol Gograd, Warsaw, Wuhan, Wuxi, Xian, Xuzhou, Yangon, Yaounde, Yerevan, Yokohama, Yoko Hama, Yoko, Hama, Zapopan, Za Po Pan, Za Popan, Zhengzhou, Zheng Zhou, Sheng Zhou, Sheng Sou, Zibo, Bangs, Soda Springs, SodaSprings, Springs, Bluff, Placentia, Fries, Dinosaur, American Fork, Concrete, Briny Breezes, Whynot, Hurt, Ninety Six, NinetySix, 96, Cut and Shoot, Cut & Shoot, CutNShoot, CutShoot, CutandShoot, Cut&Shoot, Kill Devil Hills, KillDevilHills, Devil Hills, DevilHills, Kill Devil, KillDevil, Canadian, Superior, Atomic City, Atomiccity, Atomicity, Okay, Nowhere, Hell, Coward, Three Way, ThreeWay, Threeway, Reno, Las Vegas, LasVegas, Vegas, Climax, OKC, Oklahoma City, Winnebago, Uncertain, Last Chance, LastChance, Lastchance, Speed, Oblong, Cool, Colon, Pink, BlueGrass, Blue Grass, Bluegrass, Rainbow City, RainbowCity, Rainbow, China, City, Hooker, Popejoy, London, Edinburgh, Manchester, Music City, MusicCity, Musiccity, Musicity, Memphis, Clarcksville, Nashville, Birgingham, Glasgow, Liverpool, Bristol, Oxford, Cambridge, Cardiff, Brighton, Newcastle-upon-Tyne, Newcastle, NewcastleuponTyne, NewcastleTyne, Newcastle Tyne, Tyne, Leeds, Yorkshire, York, Inverness, Culloden, Bath, Nottingham, Aberdeen, Chester, Ambrose, Amity Island, AmityIsland, Alphaville, Asteriod City, AsteroidCity, Belleville, Bedford Falls, BedfordFalls, Brahms, Brigadoon, Brightburn, Bismuth, Bristo Camino, Bristo, BristroCamino, Catsville, Chesterford, Cloverdale, Creek Falls, CreekFalls, Crystal Lake, CrystalLake, Damon, Dammuz, Deer Meadow, DeerMedow, Dillford, Dogville, Duloc, Egging, Flagstone, Fly Creek, FlyCreek, Greenbow, Greenhills, Flinthills, Green Hills, Flint Hills, Flinthill, Groom Lake City, Groom Lake, Lake City, Grouchland, Haddonfield, Harper, Hilltop, Hill Valley, HillValley, Hope, Inferno, Hope Town, Hopetown, Ivory Creek, IvoryCreek, Jonathanland, Karatas, Kartas, Khansaar, Hotha, Kotha, Liiian, Loganville, Madison, Mantua, Middleton, Midlothia, Middlesex, Millbrook, Mill Valley, Millvalley, Miles County, MilesCounty, Moesko Island, Moesko, MoeskoIsland, Mos Eisley, MosEisley, Eisley, Mos Espa, Mosespa, Espa, Mt Abraham, Mt. Abraham, MtAbraham, Mount Abraham, Newton Haven, Newton, NewtonHaven, Haven, Nickeltown, Nickles, Nilbog, Oak Ridge, OakRidge, Ogden Marsh, Ogden, OgdenMarsh, Old Stump, OlStump, Ol Stump, OldStump, Peacock, Perfection, Pleasantville, Pokyo, Portoroso, Pozharnov, Pribrezhny, Racoon City, RacoonCity, Radiator Springs, RadiatorSprings, Redmeption, Regimenton, Red Hill, Redhill, Rose Rock, Rosehill, Rockbridge, Rock Ridge, Rockridge, Rock Vegas, San Angeles, San Miguel Arcangel, San Miguel, Miguel Archangel, SanMiguel Arcangel, SanmigelArcangel, Sanford, Sandford, Santa Cecilia, Cecilia, Seabroook, Sexville, Silent Hill, Silenthill, Shermer, Silver Creek, Silvercreek, Springwood, Suburbicon, Sweetwater, Sylvane, Tenderville, Theed, Tipoca City, Tipoca, Twin Peaks, TwinPeaks, Two-Bit, 2bit, Verona, Victory, Waaji, Waaji City, WaajiCity, Wardenclyffe, Warden Clyffe, Warren Valley, WarrenValley, Woodsboro, Woop Woop, WoopWoop, Seattle, San Francisco, Francisco, Roma, Toronto, Boston, Pittsburg, Whichita Falls, Whichita, Cleveland, Denver, Jacksonville, Fort Worth, Charlotte, Columbus, Indianapolis, El Paso, ElPaso, Portland, Louisville, Baltimore, Milwaukee, Albuquerque, Tucson, Fresno, Sacramento, Mesa, Alanta, Kansas City, KansasCity, Colorado Springs, Omaha, Raleigh, Virginia Beach, Long Beach, Oakland, Bakerfield, Tulsa, Tampa, Tampa Bay, Arlington, Wichita, Wichita Falls, Aurora, New Orleans, Honolulu, Anaheim, Henderson, Orlando, Lexington, Stockton, Riverside, Corpus Christi, Irvine, Cincinnati, Santa Ana, Newark, Saint Paul, St.Paul, St Paul, St. Paul, StPaul, Durham, Lincoln, Jersey City, Plano, Anchorage, North Las Vegas, NLV, St Louis, St. Louis, New Vagas, Night City, NC, Nightcity, Madison, Chandler, Gilbert, Buffalo, Chula Vista, Fort Wayne, Lubbock, Toledo, Laredo, Irving, Chesapeake, Glendale, Winston Salem, Winston, Salem, Scottsdale, Graland, Boise, Norfolk, Spokane, Richmond, Fremont, Huntsville, Frisco, Cape Coral, Santa Clarita, San Bernardino, Tacoma, Hialeah, Baton Rouge, Modesto, Fontana, McKinney, Moreno Valley, Des Moines, Fayetteville, Salt Lake City, Salt Lake, Yonkers, Worcester, Sioux Falls, Little Rock, Amarillo, Tallahassee, Grand Prairie, Augusta, Peoria, Oxnard, Knoxville, Overland Park, Overland, Vancouver, Grand Rapids, Montgomery, Huntington Beach, Providence, Brownsville, Tempe, Akron, Chattanooga, Fort Lauderdale, Newport, Newport News, Mobile, Ontario, Cary, Elk Grove, Shreveport, Eugene, Santa Rosa, Rancho Cucamonga, Cucamonga, Pembroke Pines, For Collins, Fort Brag, Fort Sill, Springfield, Oceanside, Garden Grove, Murfreesboro, Palmdale, Corona, Killeen, Salinas, Roseville, Denton, Surprise, Macon, Paterson, Lakeood, Hayward, Charleston, Hollywood, Sunnyvalue, Sunnydale, Bellevue, Joliet, Naperville, Escondido, Bridgeport, Savannah, Olathe, Mesquite, Pasadena, McAllen, Rockford, Gainesville, Syracuse, Pomona, Visalia, Thornton, Waco, Jackson, Lakewood, Fullerton, Torrance, Victorville, Vicotoryville, Midland, Orange, Miramar, Hampton, Warren, Stamford, Cedar Rapids, Elizabeth, Palm Bay, Dayton, New Haven, Coral Springs, Meridian, West Valley City, WVC, Lewisville, Sterling Heights, Kent, Carrollton, Santa Clara, Round Rock, Roundrock, Norman, Athens, Pearland, Clovis, Topeka, College Station, Simi Valley, Allentown, Wast Palm Beach, WPB, Thousand Oaks, Vallejo, Wilmington, Rochester, Concord, Lakeland, North Charleston, Lafayette, Arvada, Independence, Billings, Ann Arbor, Broken Arrow, Indiahoma, Berkeley, Antioch, High Point, West Point, Clearwater, League City, Electric City, Evansville, Waterbury, West Jordan, Las Cruces, Westminster, Lowell, Nampa, Pompano Beach, Carlsbad, Menifee, Provo, Elgin, Greeley, Beaumont, Lansing, Murrieta, Goodyear, Allen, Tuscaloosa, Everett, Pueblo, New Braunfels, South Fulton, Miami Gardens, Grsham, Temecula, Rio Rancho, Peoria, Tyler, Sparks, Ventura, Buckeye, Downey, Sugar Land, Sugarland, Costa Mesa, Black Mesa, Area 51, Spokane Valley, Davie, Jurupa Valley, Centennial, Edison, Boulder, Dearborn, Edinburg, Hesperia, Suffolk, Yuma, Lynn, Quincy, Palm Coast, Vacaville, Florance, Annecy, Amsterdam, Mykonos, Valletta, Tallinn, Lisbon, Strasbourg, Ghent, Dubrovinik, Reykjavik, Lucerne, Galway, Barsov, Aarhus, Vilnius, Split, Bordeaux, Marseille, Innsburk, Farnkfurt, Santorini, Brussels
 
##### Metropolis: 
###### Agrabah, Alantica, Autobot, Autobot City, AutobotCity, Auto Bot City, Cloud City, CloudCity, Emerald City, EmeraldCity, Mega City, Megacity, Mega-City, Mega-City One, Mega-City 1, Megacity 1, Megacity1, Metropolis, Metroville, Monstropolis, Ratropolis, Zion, Croix-des-Bouquets, Croix des Bouquets, Croix Bouquets, Giza, Manila, Mandaluyong, Male, Dhaka, Bnei Brak, Caloocan, Kolkata, Kathmandu, Makati, Levallois Perret, Guediawaye, Montouge, Bogota, Vincennes, Le Pre Saint Grevais, Pre Saint Grevias, Le Pre St Grevais, St Grevais, Saint Grevais, Pasig, Saint Mande, St Mande, St. Mande, St. Grevais, Le Pre St. Grevias, Pre St. Grevias, La Planta, Planta, Saint Josse ten Noode, St Josse ten Noode, St Josse, St. Josse, Saint Josse, Guttenberg, Malabon, Pasay, Neapolli, Damascus, San Juan, SanJuan, Navotas, Asmara, Mislata, Macau, Kaillithea, Nea Smyrni, NeaSymrni, Union City, Colombo, L'Hospitalet, L'Hositalet de Llobregat, Llobregat, Marikina, Saint Gilles, St. Gilles, Clichy, Kotsibuynske, Boulogne-Billancourt, Boulogne Billancourt, Boulonge, Billancourt, Giv'atayim, Givatayim, Las Pinas, LasPinas, Pinas, Koekelberg, Bandung, General Mariano Alverez, Mariano Alverez, GMA, Monaco, Les Lilas, LesLilas, Lilas, Hoboken, Pikine, Quezon, Quezon City, Quezoncity, Modi'in Illit, Modi'in, Illit, Vanves, Asnieres sur Seine, AsnieresSurSiene, Ciudad, Cidad Nezahulcoyotl, Nezahlcoyotl, Silema, Howrah, Santa Coloma de Gramenet, Chittagong, Sint Jans Molenbeek, Keur Massar, KeurMassar, Charenton le Pont, La Garenne Colombes, Schaerbeek, Neuilly sur Seine, Issy les Moulineaux, Moulineaux, Jakarta, Bat Yam, Batyam, Gentilly, Cario, Mandaue, Warabi, Bacoor, El'ad, Beitar Illit, Elad, Senglea, Cimahi, San Pedro, Lagos, Kiryat Motzkin, Gaza City, Geneva, Portici, Chongqing, Bengaluru, Ahmedabad, Dongguan, Miami, Atlanta, Washington, Washinton DC, DC, Jinan, Guadalajara, San Jose, SanJose, Detroit, Minneapolis, Antwerp, Athena, Greater Bristol, Dnipro, Gdansk, Tricity, Gothenburg, Hauge, Hannover, Helsinki, Katowice, Karkow, Kyiv, Lille, Lisborn, Lodz, Lyon, Malaga Marbella, Marbella, Mannheim Ludwigshafen, Ludwigshafen, Mannheim, Milan, Naples, Nantes, Nice, Bremen, Nuremberg, Oslo, Ostrava, Poznan, Rhien Nord, Dusseldorf, Neuss, Rhein Sud, Cologne, Bonn, Riga, Rotterdam, Ruhr, Saarbrucken, Forbach, Saratov, Seville, South Yorkshire, Stuttgrat, Toulouse, Turin, Tyne and Wear, Wear, Voroenzh, West midlands, Zagreb, Zurich, Randstad, Flemish, Flemish Diamond



### &nbsp; &nbsp; Personality Traits
##### Goal Driven: 
###### Idoit, Independent, Jack-Of-All-Trades, Leader, Entrepreneur, Realist, Optimistic, Slacker, Loner, Outcasted

##### Socially Driven: 
###### Influencer, Follower, Worker, Idealist, Pessimistic

##### Simply Driven: 
###### Faithful, Unfaithful, Neutral, Trustworthy, Untrustworthy

##### Belief Driven: 
###### Druid, Jewish, Catholic, Christian, Muslim, Pegan, Spiritualist, Revolutionist, Atheist, Satosist, Stateist

##### Culture Driven: 
###### Punk, S.P.A.M., McCreedy, Goth, Fashion Goth, Nerd, Dork, Geek, Tri-Alpha-Phi-Delta, Jock, Cheerleader, Pop Cultered, Fashion Sub-Cultered, Sub-Cultered, Alt-Cutlered

##### Thought Driven: 
###### Scientologist, Alien Hopeful, Alien Waiter, Alien Denier, Alien Hater, Abductee, Abductor, Abducted

##### Knowledge Driven: 
###### Anti-Mancer, Solo-Mancer, Dual-Mancer, Tri-Mancer, Multi-Mancer, Forever Mancer

##### Physically Driven: 
###### Human, Synthetic, Droid, Alien, Monster, Zombie, Fairy, Cryptid, Gold-Bug, Crusader, Gold-Digger, Cougar, Prey, Lion, Stud, Stead, Pony, Furry, Bear, Ox, Bull, Bat

##### Digitally Driven: 
###### range, Silver, Grey, Bitcoiner, No-Coiner, Altcoiner, All-Coiner, Spammer, Bot



### &nbsp; &nbsp; Perspective Ideas
##### Motivational: 
###### Sloth, Procrastinator, Almost On-Time, On-Time, Occasionally Early, Early Bird

##### Educational: 
###### Never Been, Occasionally Visited, Average Student, Above Average, Exceptional, Home Learned

##### Technological: 
###### Stays Away, Sometimes Uses, Commonly Uses, Normally On-Hand, On-Hand, Always Available

##### Traditional: 
###### Modern, Tech Modern, Evenly Mixed, More Traditional, Very Traditional, Traditional

##### Governmental: 
###### Marxism, Socialism, Dictatorship, Boarded Republic, Family Monarchy, Democratic Republic

##### Personal: 
###### It’s All About Me, Me & Mine, Help Yourself then Others, Help Others First, It’s about Us not We, It Takes A Village



### &nbsp; &nbsp; Positive Bonds
##### Active: 
###### Accepting, Active, Adventurous, Athletic, Attentive, Captivating, Charismatic, Cheerful, Competent, Daring, Dedicated, Dutiful, Earnest, Ebullient, Energetic, Enthusiastic, Faithful, Grateful, Gregarious, Hardworking, High-Spirited, Humorous, Observant, Neat, Outgoing, Playful, Productive, Punctual, Quirky, Reliable, Responsive, Seraphic, Serious, Sociable, Spontaneous, Tidy, Vivacious, Youthful, Zealous

##### Assertive: 
###### Assertive, Assured, Balanced, Blunt, Brilliant, Consistent, Convincing, Decisive, Determined, Diligent, Driven, Encouraging, Extraordinary, Felicific, Firm, Forceful, Guileless, Heroic, Honest, Independent, Individualistic, Intuitive, Paternalistic, Persistent, Persuasive, Protean, Prudent, Disciplined, Suave, Talkative, Urbane

##### Dynamic: 
###### Adaptable, Admirable, Alert, Appreciative, Capable, Chummy, Cultured, Dignified, Dynamic, Fashionable, Flexible, Gallant, Insightful, Intelligent, Outspoken, Resilient, Resourceful, Rounded, Versatile

##### Bold: 
###### Ambitious, Authentic, Bold, Brave, Clever, Confident, Courageous, Creative, Forthright, Frank, Hearty, Humble, Interesting, Loyal, Obedient, Original, Responsible, Skilled, Venturesome

##### Paced: 
###### Breezy, Cautious, Charming, Conciliatory, Cooperative, Crafty, Diplomatic, Dreamer, Elegant, Eloquent, Fair, Focused, Mannered, Optimistic, Open-Minded, Paced, Proficient, Quiet, Reserved, Stoic, Trustworthy, Well-Read

##### Calm: 
###### Affable, Calm, Clear-Headed, Easygoing, Friendly, Placid, Patient, Rational, Relaxed

##### Methodical: 
###### Accurate, Articulate, Artistic, Careful, Clean, Constructive, Contemplative, Discreet, Efficient, Esthetic, Ethical, Knowledgeable, Logical, Lyrical, Methodical, Meticulous, Multi-Leveled, Orderly, Organized, Precise, Perfectionist, Pragmatic, Purposeful, Scholarly, Scrupulous, Shrewd, Sophisticated, Systematic, Tolerant, Understanding

##### Thoughtful: 
###### Allocentric, Bright, Broad-minded, Compassionate, Conscientious, Considerate, Curious, Dependable, Empathetic, Freethinking, Helpful, Honorable, Imaginative, Incisive, Innovative, Inventive, Kind, Magnanimous, Mindful, Perceptive, Practical, Realistic, Reflective, Studious, Sympathetic, Thoughtful, Thrifty, Wise, Witty

##### Emotional: 
###### Affectionate, Amusing, Benevolent, Caring, Congenial, Courteous, Debonair, Deep, Dramatic, Emotional, Empathetic, Exuberant, Expressive, Fancy, Forgiving, Fun-Loving, Funny, Generous, Gentle, Genuine, Giving, Good-Natured, Gracious, Happy, Hopeful, Insouciant, Lovable, Loving, Mature, Mellow, Nurturing, Open, Passionate, Patriotic, Peaceful, Personable, Philanthropic, Polite, Positive, Progressive, Protective, Proud, Reasonable, Respectful, Romantic, Rustic, Sensitive, Sentimental, Sharing, Sincere, Supportive, Trusting, Warm, Wholesome



### &nbsp; &nbsp; Negative Flaws
##### Active: 
###### Active, Angry, Argumentative, Barbaric, Boisterous, Brutal, Clumsy, Disconcerting, Disrespectful, Discourteous, Disorderly, Disturbing, Fraudulent, Harsh, Hesitant, Hidebound, Ignorant, Impulsive, Inconsiderate, Indulgent, Intolerant, Libidinous, Mannerless, Misguided, Mistaken, Narrow-Minded, Negativistic, Nihilistic, Pedantic, Perverse, Pompous, Reactive, Reckless, Ridiculous, Rude, Rowdy, Sarcastic, Stupid, Suspicious, Thoughtless, Troublesome, Unforgiving, Unreliable, Vulgar

##### Assertive: 
###### Abrasive, Abrupt, Aggressive, Assertive, Bossy, Blunt, Cantankerous, Closed-Minded, Condemnatory, Crazy, Criminal, Demanding, Devious, Discouraging, Disputatious, Disruptive, Domineering, Enervated, Envious, Fawning, Forceful, Greedy, Hostile, Inhibited, Insulting, Irascible, Irritable, Imitative, Impatient, Manipulative, Mealy-Mouthed, Meddlesome, Narcissistic, Obsessive, Opinionated, Overbearing, Passive-Aggressive, Possessive, Power-Hungry, Predatory, Provocative, Puritanical, Rigid, Temperamental, Uncooperative, Unfriendly, Vindictive, Violent, Vulnerable

##### Dynamic: 
###### Artificial, Asocial, Boorish, Disloyal, Disobedient, Dynamic, Erratic, Flaky, Impulsive, Neurotic, Obnoxious, Pharisaical, Pugnacious, Unrestrained, Unstable, Vague

##### Bold: 
###### Arrogant, Bizarre, Bold, Conceited, Challenging, Compulsive, Crass, Decadent, Destructive, Dishonest, Dogmatic, Faithless, Fanatical, Haughty, Intense, Irreverent, Malicious, Mawkish, Meretricious, Profligate, Scornful, Sly, Stubborn, Treacherous, Unpredictable, Unlovable, Venomous

##### Paced: 
###### Aimless, Cautious, Cowardly, Distractible, Gullible, Lazy, Loquacious, Inert, Messy, Muddle-Headed, Naive, Neglectful, One-Dimensional, Self-Centered, Paced, Plodding, Sadistic, Sedentary, Shallow, Sloppy, Softheaded

##### Calm: 
###### Aloof, Amoral, Apathetic, Bland, Calm, Careless, Confused, Disorganized, Discouraged, Incurious, Insensitive, Monstrous, Natty, Selfish, Slovenly, Unreflective, Vacuous

##### Methodical: 
###### Contemptible, Deceitful, Deceptive, Dissolute, Expedient, Fickle, Finicky, Imprudent, Picky, Pragmatic, Mannered, Mechanical, Methodical, Scheming, Secretive, Sneaky, Superstitious, Thievish, Unrealistic, Venal

##### Thoughtful: 
###### Cruel, Cynical, Forgetful, Indecisive, Mischievous, Nervous, Pessimistic, Stingy, Superficial, Thoughtful, Uncertain, Unctuous

##### Emotional: 
###### Afraid, Anxious, Bewildered, Callous, Childish, Cold, Complacent, Complaining, Delicate, Dependent, Desperate, Discontented, Dull, Egocentric, Emotional, Fatalistic, Fearful, Fiery, Frightening, Frivolous, Gloomy, Grim, Hateful, Hedonistic, Insecure, Insincere, Irrational, Irresponsible, Jealous, Judgmental, Miserable, Moody, Needy, Paranoid, Petty, Phlegmatic, Prim, Regretful, Repentant, Resentful, Surly, Sanctimonious, Steely, Stiff, Tense, Vain, Weak, Wishful


### &nbsp; &nbsp; Item Importing (Data Commands)
###### import, download, install, mount, collect, item



### &nbsp; &nbsp; World Timer Commands (Data Commands)
###### wtreset, wtoff



### &nbsp; &nbsp; Scrollbar Commands (Data Commands)
###### fixscroller, scrolliseverything, scrollingitems, showlicense, changescroller



### &nbsp; &nbsp; Wallet UX (Online Commands):
###### send, transfer, utxo, unspent, transactions, transact, p2p, hotswap, bip, bitcoin



### &nbsp; &nbsp; Wallet UI (Online Commands):
###### coin, catch, blockchain, fetch, crypto, sweep, virtualmachine, proofofstake, proofofwork



### &nbsp; &nbsp; Bank & Exchange (Online Commands)
###### spend, forex, casino, gamble, exchange, trade, markets, bank, hotswap, xrp, cdbc, marketcrash



### &nbsp; &nbsp; General Commands (Print Commands)
###### resetlevel, rosebud



#### &nbsp; &nbsp; &nbsp; &nbsp; Recgonized Words/Commands: 2700+ unique words recgonized
---

---
## iCS Input Sanatization Process'

### &nbsp; &nbsp; Because there is a <q><i>Click-to-Change</i></q> mechanic, there are a series of sanatizers. Each one handles things slightly differently for different reasons but we could drop these down to essentially 3 sanatizers.



### &nbsp; &nbsp; Spell & Standard Input Sanatizer:
###### Used with a replacement function: <code>/[^a-z0-9áéíóúñü\[\] \'@#&.,_-]/gim</code> ***JavaScript RegEx***
###### This design doesn't allow for much more than important writable characters. This should prevent links & javascript manipulation in the input field.



### &nbsp; &nbsp; Document Sanatizer:
###### Used with a replacement function: <code>/[^a-z0-9áéíóúñü\[\] \'@#&.,_-]/gim</code> ***JavaScript RegEx***
###### Using the same as the spell sanatizer but this is implimented at 3 lines at a time, which is max lines size for writable documents in iCS. This should prevent links & javascript manipulation in the input field.



### &nbsp; &nbsp; Numbers 1 Sanatizer:
###### Used with a replacement function: <code>/(/[^0-9 \-]/gim</code> ***JavaScript RegEx***
###### This should only allow numbers (no decimals) but should allow for negative numbers in the input field.



### &nbsp; &nbsp; Numbers 2 Sanatizer:
###### Starting at the replacement function: <code>input = input.replace(/[^0-9\.]/gim,"");</code>
 
###### <code> if(input.toString().toString().search(/\./gm) >= 0){</code>
###### <code>  if(input.toString().match(/\./gm).length >= 2){</code>
###### <code>   var tempinput = input.split(/\./g)[0] + "." + input.split(/\./g)[1] + input.split(/\./g)[2].replace(/[^0-9]/gim,"");</code>
###### <code>   input = tempinput; } }</code> ***JavaScript Snippet***
###### This should only allow numbers (with decimals) while keeping out negative numbers in the input field.

---
--
--
--
---

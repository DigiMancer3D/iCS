# iCS
### An interactive Character Sheet with a custom open ended "Unlicense"
---

To play with iCS live, visit https://3dd.in/iCS or the use IFPS CID directly #QmNVmZ5LmRHnypPw8QDJYATGj6wxaRSspTQYYo1LS2SC5U to view, use & host



## About iCS::


&nbsp;&nbsp;&nbsp; The interactive Character Sheet was first built up by 3Douglas "<i>3D</i>" Pihl. Because the Open Gaming License (pre OGL 2) was looking at being changed by Hasbro via Wizards of the Coast. Because of the hurt this would cause, many people (VTT and Table Top Players) very quickly begun changing to adapt to the unforturnate events by these conglomerates. Out of that madness, 3D began working on an online usable Character Sheet. With a non-static character sheet not reliant upon the OGL licensing, this could help people continue to enjoy their favorite table top, RPG or larping online without worry. Using Itty-Bitty v1 to create personalized iCS saves that allows for people to send, trade or continue previous saves. Wave Data APIs are used for sending objects into and out-of the interactive Character Sheet (iCS).


&nbsp;&nbsp;&nbsp; iCS takes cares of many actions for the users and considerations in a manner that is based on a custom RPG layout concept. Where OGL DnD may be mostly based upon common logic consideration & Pathfinder could be considered more Mathematical logical considersations, while both are relaint on rolls for checks. iCS uses a combination of both common logic & mathematical logical considerations & uses equational checks & rolls for randomizing possibilities. The internal algos help make the process of keeping up with a character sheet easy for all user levels, from handling equip allowances to determining if you are overburden. Almost every aspect that isn't strictly player choice, has been reduced to alorithms & equations. The algorithms used are as follows:

## Input Maker: This algorithm inserts an input with some customized information per area called for an input. This allows for anything on the page that can be changed just needs the user to click to be able to change it.

## Weight: This algorithm considers the estimated weight of items based on their item type. When a player becomes over-burdened, an orange OB will appear next to the Armor words. If a player is too underweight (overweight will be coming with this feature soon), they can becomed overburdened easier or even be unable to sustain their own weight (with armor, weapons, etc) which can cause loss of carry capability as well as loss of health points.

## Backfill1: This will return data from instered inputs back to where they were but with the inputted data as new information.
</br>

--
## Holding: This algorithm looks at how many items are being held when equiping and unequiping holdables (like weapons and books).
### &nbsp; IF: A player that has strength that's higher then their strength combined with their phyiscal dexterity divided by their mental dexterity adjust up by 45 points can hold 2-handed items simultaneously.   
#### &nbsp; &nbsp; &nbsp; "((S+PDex)/(Mdex))+45 <= strength" === Duel Wielding 2H Weapons
 
### &nbsp; THEN: If your character meets this criteria, equip a single handed object then equip a 2-handed weapon.
#### &nbsp; &nbsp; Once equpied, unequip the 1-handed object then equip a second 2-handed weapon.  
#### &nbsp; &nbsp; &nbsp; 1H -> Hold Check (duel opened) -> 2H -> unequip 1H -> equip 2H (check not needed)
--

---
## User Details: This algorithm is a set of algorithms that keep track of various user character data.
 ### &nbsp; &nbsp; Armor Points: Points that represents the character's armor.
 ### &nbsp; &nbsp; Defense Points: Points that represents the character's attack power.
 ### &nbsp; &nbsp; Health Points: The number of points the user can take before dieing.
 ### &nbsp; &nbsp; Experience Points: The amount of total and active user experience points. 
 ### &nbsp; &nbsp; Inspirations: Revalations by the character based on a random roll & other factors.
 ### &nbsp; &nbsp; Player Weight: Tracks player weight <code>[lbs.oz]</code>.
 ### &nbsp; &nbsp; Player Height: Tracks player height <code>[feet.inches]</code>.
 ### &nbsp; &nbsp; Player Ratio: Tracks players weight:height <code>[feet.inches]</code> ratio. 
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

## Item Rebuilding: The return API that tells how to rebuild the item via the hash.
<hr>


# Unique Actions with iCS

--
## Contracting (Bountys & Writing)

### &nbsp; Writing a contract for a bounty can allow you to hire for these actions. The Contracts also handle the writing actions for making journal entries and deeds for items/property/objects.

#### &nbsp; &nbsp; All bounties are based on on-game trust but do not turst the bounty writer for anything is possible.

#### &nbsp; &nbsp; Objects writen in your writables are not being seen by others.
   
#### &nbsp; &nbsp; Importing Items

### &nbsp; If you have an item hash from another player or round, you can import the item as old-new. This can allow you to transfer items across games with just a hash or save usable game items for a list or database for all players to have all the same item data.

#### &nbsp; &nbsp; This can also allow for users to transfer messages or contracts for a new layer of player actions.

### &nbsp; Pressing the "s" button below each item will give the current status of that item as a hash. This hash can be shared and anyone with that hash can import that item. This is for side-layer player actions, player contracts, debts, and for onlline table-top gaming.

### &nbsp; To import an item from an item hash, click "Add Item" then insert, "print" into the first input field and then insert, "import" or another import type action command to activate the importing input. Place the item hash in that blank input and click, "Add" to add that item.

### &nbsp; &nbsp; &nbsp; If an item's code is malformed from transferring, recieving users may have to click a final item type button.
--

--
## Import:

#### &nbsp; &nbsp; &nbsp; Add Item --> "drive" --> "import" --> item importer

### &nbsp; :To Access:   
### &nbsp; &nbsp; :Item Importer:
### &nbsp; &nbsp; Input 1 --> "Drive"
### &nbsp; &nbsp; Input 2 --> "import"
### &nbsp; &nbsp; What you get --> Item Importer App

## &nbsp; **Do Not Import Funds This Way**
--

--
## Books (Reading VS Holding)

   Some books are held to gain acces to item's attribute de/booster. While other books are a one time reading action. Scrolls, pages, books and similar may be considered "readables" which are all conted as 'books'.

### &nbsp; &nbsp; Hoover to learn more about most actions.
--

--
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
--

--
## Commands

### &nbsp; &nbsp; Comands are put in the first two inputs after clicking to "Add Item". The first input commands are normally names of items. This section also does internal triggering but there's three other user commands possible, "data", "print" & "online". Data, Print & Online are unimportant commands but are helpful for users remembering the options for the next set of commands.

### &nbsp; &nbsp; The second set of input commnads are normally item types but there are a handful of recognized commands that perform various actions like access the Banking app, the Crypto wallet & Cheats. In the list of recgonized inputs, unless they say "trigger" or are for "triggers" then they work on this line of commands. Going through that list will help you navigate around the iCS application.

#### &nbsp; &nbsp; &nsbp; Most commands will work under this process tree: command1, command2, command3*, command-expander*.

--
## Input Process Trees

### &nbsp; :Item:
##### &nbsp; &nbsp; &nbsp; Name -- Type* -- Details* -- Extras* -- Hash*

### &nbsp; &nbsp; :Data:
### &nbsp; &nbsp; "Data" -- Command -- Hash* -- De/Encoder

### &nbsp; :Internet:
### &nbsp; &nbsp; "Online" -- Command -- Hash* -- De/Encoder

#### &nbsp; &nbsp; * an astrik represents an injection possible point
#### &nbsp; &nbsp; &nbsp; " " words inside quotation marks are verbatim command input
--

--
## Unlocked License (UnLicense)

### &nbsp; &nbsp; The Unlocked License is a form of License that has only 2 stimpulations for validity, which are as follows:

#### &nbsp; &nbsp; 1) If previous credits are available & visiable without clicking anything or going anywhere.
#### &nbsp; &nbsp; 2) if this license is available & visiable with a maximum of a single click or without any clicking.

### &nbsp; &nbsp; The Unlocked License uses predetermined clauses to consider if the license and the use of the license is valid. To determine if this license is valid follow these stimpulations, which are as follows:
###### Credit to the previous workers, builders, originators and others involved with the web object/app/page/document and it's content before & of the current version of the web object/app/page/document & content must be visiable without any clicking, hiding behind any button, object, terms of service, conditions, terms, color-blending, background hiding, font color hiding or otherwise that is not directly viewable by users.
This license must be visiable with a maximum of a single click mechanic, a single linked page (must be a direct to page or direct to file link) or directly on the page to the users.

###### If this license is valid, then this web object/app/page/document & the use of this web object/app/page/document is allowed by this license. If this license is not valid, then the web object/app/page/document & use of this web object/app/page/document is not allowed. If the original credit & any additional credits are left in-tact and are visible as previously described in this license, then this license is valid. If this license is visible either through a single click mechanic, a single linked page (must be a direct to page or direct to file link) or directly on the page then this license is valid.

###### No user specific data is allowed to transfer to new users, owners, builders, creators or any other enitity, person, company, governemnt or electronic identity or intelligence. This license is over the usability and the web object/app/page/document itself not the user-specific data inputted, automated, generated or processed from use of the web object/app/page/document. The user that inputs data as well as causes the creation of data through automation, generation, APIs or processing is for that user alone. This does not mark owners of data inputted, automated, generated, pulled in, proccessed or considered but does deny the builders, creators, hosts, interactors of the web object/app/page/document allowance of being called owners of any data inputted, automated, generated, pulled in, proccessed or considered through this or any future version of this web object/app/page/document. This license cannot be revoked, removed, changed or withdrawn without causing the license for that specific version of the web object/app/page/document. To stop using this license for future versions of the connected web object/app/page/document, you will have to create a new version of this web object/app/page/document without this license but must include that the new version is not an Unlocked License Web Object in a clear, readable format that's directly viewable by users without any clicking or hiding of any kind.
--

--
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


#### &nbsp; &nbsp; &nbsp; &nbsp; Recgonized Words/Commands: 1100+ unique words recgonized
--

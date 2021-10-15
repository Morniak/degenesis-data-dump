# degenesis-data-dump

Data extracted from the DEGENESIS [book](https://degenesis.com/downloads/books) and [website](https://degenesis.com).

Degenesis® is TM SIXMOREVODKA Studio GmbH. All rights reserved. This is a 100% non-profit community fanwork project. Before using the data in this repository, please make sure you usage is permited by the SIXMOREVODKA & DEGENESIS fan work policy.

If you like my work, consider [making a donation](https://degenesis.com/support-us) to SIXMOREVODKA.

## Icons

- `all-icons-urls.txt`: A list of all the icon pages urls. One url peer page, 253 lines.
- `all-icons-image-urls.txt`: A list of all the icon image urls. Can be easily used by with a download manager or a shell script to retrive locally all the images. The file names will match the `image_name` field of the `.json` files. 
- `Icons/json/`: One `.json` file per Icon. 

Exemple of `.json` file:

```JSON
{
    "area_of_operations": "Franka, Bayonne",
    "bio_href": "/world/bio/apocalyptics/sacrocant",
    "bio_url": "https://degenesis.com/world/bio/apocalyptics/sacrocant",
    "concept": "The Ruler",
    "connected_to": [
        {
            "href": "/world/icons/spitalians/charcutier",
            "image_name": "icons-charcutier.jpg",
            "name": "Charcutier"
        }
    ],
    "cult": "Apocalyptics",
    "culture": "Franka",
    "image_name": "icons-sacrocant.jpg",
    "image_url": "https://img2.storyblok.com/1492x0/filters:quality(90)/f/72501/2000x2000/d22b457f91/icons-sacrocant.jpg",
    "last_seen": "2596",
    "name": "Sacrocant",
    "rank": "Raven",
    "source": [
        "Rising Ravens",
        "The Killing Game"
    ],
    "source_url": "https://degenesis.com/world/icons/apocalyptics/sacrocant",
    "summary": "The Raven and undisputed ruler of Bayonne. He has converted a bogged down Surge Tank in the Rh\u00f4ne swamps into his Flock\u2019s nest.",
    "url_name": "sacrocant"
}
```

## Profiles

- `*-profiles-raw.text`: One file per book. Each entry is separated by an empty line. The profile name is between two `~~~` symbols. See the exemple below.
- `*-profiles.json`: A `.json` representation based on the `*-profiles-raw.text` files. 

Exemple of `raw.text` file:
```
...

~~~BELMONDO~~~
ARCHETYPE: Purgare, The Visionary, Clanners: Defilers, Rank X: Tainted One
ATTRIBUTES: BOD: 4 AGI: 2 CHA: 1 INT: 1 PSY: 1 INS: 4
SKILLS: Athletics 5D, Brawl 7D, Force 9D, Melee 8D, Stamina 8D, Toughness 9D, Crafting 4D, Mobility 4D, Stealth 3D, Conduct 2D, Legends 3D, Cunning 2D, Domination 5D, Reaction 3D, Willpower 3D, Orienteering 9D, Perception 7D, Primal 7D, Survival 8D
BACKGROUNDS: Secrets 4
SPECIAL: Branded (Murderer); Access to the Knacker’s Office, who pay a pittance of Drafts for any vermin corpses he drags in. The real payoffs are human corpses - Belmondo is given 25 Drafts for each one
POTENTIALS: Elephant Skin 2, Danger Sense 1
INITIATIVE: 3D / 14 Ego (Primal)
ATTACK: Spiked Club, Melee 7D, Distance 2m, Damage 10, Impact (2T), Entangled (-2D), Gruesome (2)
DEFENSE: Passive 1; Melee active (Parry), Melee 7D; Ranged Combat active, Mobility 4D; Mental, Willpower 3D
MOVEMENT: 5m
ARMOR: Rags over elephant skin, Armor 2 (-2D on CHA+Seduction)
CONDITION: Spore Infestation 1/6, Flesh Wounds 18, Trauma 5
SPECIAL EQUIPMENT: Flashlight; Liquor bottle; 1D animal carcasses; Poorly mixed black powder (used to make explosive traps for vermin, Damage 4, Camo (3C), Explosive); Bar of surplus soap

...
```

Exemple of `.json` profile:
```JSON
{
    "Belmondo": {
        "archetype": {
            ".raw-value": "Purgare, The Visionary, Clanners: Defilers, Rank X: Tainted One",
            "clan": "Defilers",
            "concept": "The Visionary",
            "cult": "Clanners",
            "culture": "Purgare",
            "rank": "Rank X: Tainted One"
        },
        "armor": "Rags over elephant skin, Armor 2 (-2D on CHA+Seduction)",
        "attack": "Spiked Club, Melee 7D, Distance 2m, Damage 10, Impact (2T), Entangled (-2D), Gruesome (2)",
        "attributes": {
            ".raw-value": "BOD: 4 AGI: 2 CHA: 1 INT: 1 PSY: 1 INS: 4",
            "agi": "2",
            "bod": "4",
            "cha": "1",
            "ins": "4",
            "int": "1",
            "psy": "1"
        },
        "backgrounds": {
            ".raw-value": "Secrets 4",
            "allies": 0,
            "authority": 0,
            "network": 0,
            "renown": 0,
            "resources": 0,
            "secrets": 4
        },
        "condition": {
            ".raw-value": "Spore Infestation 1/6, Flesh Wounds 18, Trauma 5",
            "flesh-wounds-current": 18,
            "flesh-wounds-max": 18,
            "spore-infestation-current": 1,
            "spore-infestation-max": 6,
            "trauma-current": 5,
            "trauma-max": 5
        },
        "defense": "Passive 1; Melee active (Parry), Melee 7D; Ranged Combat active, Mobility 4D; Mental, Willpower 3D",
        "initiative": "3D / 14 Ego (Primal)",
        "movement": "5m",
        "potentials": {
            ".raw-value": "Elephant Skin 2, Danger Sense 1",
            "0": "Elephant Skin 2",
            "1": "Danger Sense 1"
        },
        "skills": {
            ".raw-value": "Athletics 5D, Brawl 7D, Force 9D, Melee 8D, Stamina 8D, Toughness 9D, Crafting 4D, Mobility 4D, Stealth 3D, Conduct 2D, Legends 3D, Cunning 2D, Domination 5D, Reaction 3D, Willpower 3D, Orienteering 9D, Perception 7D, Primal 7D, Survival 8D",
            "artifact-lore": "1",
            "arts": "1",
            "athletics": "5",
            "brawl": "7",
            "conduct": "2",
            "crafting": "4",
            "cunning": "2",
            "deception": "1",
            "dexterity": "2",
            "domination": "5",
            "empathy": "4",
            "engineering": "1",
            "expression": "1",
            "faith": "1",
            "focus": "1",
            "force": "9",
            "leadership": "1",
            "legends": "3",
            "medicine": "1",
            "melee": "8",
            "mobility": "4",
            "navigation": "2",
            "negotiation": "1",
            "orienteering": "9",
            "perception": "7",
            "primal": "7",
            "projectiles": "2",
            "reaction": "3",
            "science": "1",
            "seduction": "1",
            "stamina": "8",
            "stealth": "3",
            "survival": "8",
            "taming": "4",
            "toughness": "9",
            "willpower": "3"
        },
        "special": "Branded (Murderer); Access to the Knacker’s Office, who pay a pittance of Drafts for any vermin corpses he drags in. The real payoffs are human corpses - Belmondo is given 25 Drafts for each one",
        "special-equipment": {
            ".raw-value": "Flashlight; Liquor bottle; 1D animal carcasses; Poorly mixed black powder (used to make explosive traps for vermin, Damage 4, Camo (3C), Explosive); Bar of surplus soap",
            "0": "Flashlight",
            "1": "Liquor bottle",
            "2": "1D animal carcasses",
            "3": "Poorly mixed black powder (used to make explosive traps for vermin, Damage 4, Camo (3C), Explosive)",
            "4": "Bar of surplus soap"
        }
    },
    "...": { }
}
```

# Request Response Cycle, APIs, and Postman Lab

You will be working with a free API of your choice for this lab.

## Getting Started

1. Choose an API that has no auth and no CORS from the following list: [public APIs](https://github.com/public-apis/public-apis)
1. Write your answers in this README.md file. Do not delete the questions. Write your answers after the `>`. If you need to write more than one paragraph, add more `>`.

## Instructions

Do your best to answer the questions with specific details when required fully. Writing about code clearly and thoroughly is a critical skill to practice. 

- Which one did you choose? Provide the name and base URL

> https://www.dnd5eapi.co/

- What purpose is this API for (education/fun and games/information/etc.)?

> The purpose of this API is for the table top game Dungeons and Dragons. It holds information about the monsters, spells, and etc.

- What is the URL of the documentation?

> https://www.dnd5eapi.co/docs/

- What is the full URL of one endpoint?

> https://www.dnd5eapi.co/api/monsters/adult-black-dragon/

- What is a sample of the data from the endpoint (copy and paste results from Postman, ok to shorten if it’s over 100 lines)? Be sure to wrap your answer in the correct formatting for code/JSON.

```json
{
    "index": "adult-black-dragon",
    "name": "Adult Black Dragon",
    "size": "Huge",
    "type": "dragon",
    "alignment": "chaotic evil",
    "armor_class": [
        {
            "type": "natural",
            "value": 19
        }
    ],
    "hit_points": 195,
    "hit_dice": "17d12",
    "hit_points_roll": "17d12+85",
    "speed": {
        "walk": "40 ft.",
        "fly": "80 ft.",
        "swim": "40 ft."
    },
    "strength": 23,
    "dexterity": 14,
    "constitution": 21,
    "intelligence": 14,
    "wisdom": 13,
    "charisma": 17,
    "proficiencies": [
        {
            "value": 7,
            "proficiency": {
                "index": "saving-throw-dex",
                "name": "Saving Throw: DEX",
                "url": "/api/proficiencies/saving-throw-dex"
            }
        },
        {
            "value": 10,
            "proficiency": {
                "index": "saving-throw-con",
                "name": "Saving Throw: CON",
                "url": "/api/proficiencies/saving-throw-con"
            }
        },
        {
            "value": 6,
            "proficiency": {
                "index": "saving-throw-wis",
                "name": "Saving Throw: WIS",
                "url": "/api/proficiencies/saving-throw-wis"
            }
        },
        {
            "value": 8,
            "proficiency": {
                "index": "saving-throw-cha",
                "name": "Saving Throw: CHA",
                "url": "/api/proficiencies/saving-throw-cha"
            }
        },
        {
            "value": 11,
            "proficiency": {
                "index": "skill-perception",
                "name": "Skill: Perception",
                "url": "/api/proficiencies/skill-perception"
            }
        },
        {
            "value": 7,
            "proficiency": {
                "index": "skill-stealth",
                "name": "Skill: Stealth",
                "url": "/api/proficiencies/skill-stealth"
            }
        }
    ],
    "damage_vulnerabilities": [],
    "damage_resistances": [],
    "damage_immunities": [
        "acid"
    ],
    "condition_immunities": [],
    "senses": {
        "blindsight": "60 ft.",
        "darkvision": "120 ft.",
        "passive_perception": 21
    },
    "languages": "Common, Draconic",
    "challenge_rating": 14,
    "xp": 11500,
    "special_abilities": [
        {
            "name": "Amphibious",
            "desc": "The dragon can breathe air and water."
        },
        {
            "name": "Legendary Resistance",
            "desc": "If the dragon fails a saving throw, it can choose to succeed instead.",
            "usage": {
                "type": "per day",
                "times": 3,
                "rest_types": []
            }
        }
    ],
    "actions": [
        {
            "name": "Multiattack",
            "multiattack_type": "actions",
            "desc": "The dragon can use its Frightful Presence. It then makes three attacks: one with its bite and two with its claws.",
            "actions": [
                {
                    "action_name": "Frightful Presence",
                    "count": 1,
                    "type": "ability"
                },
                {
                    "action_name": "Bite",
                    "count": 1,
                    "type": "melee"
                },
                {
                    "action_name": "Claw",
                    "count": 2,
                    "type": "melee"
                }
            ]
        },
        {
            "name": "Bite",
            "desc": "Melee Weapon Attack: +11 to hit, reach 10 ft., one target. Hit: 17 (2d10 + 6) piercing damage plus 4 (1d8) acid damage.",
            "attack_bonus": 11,
            "damage": [
                {
                    "damage_type": {
                        "index": "piercing",
                        "name": "Piercing",
                        "url": "/api/damage-types/piercing"
                    },
                    "damage_dice": "2d10+6"
                },
                {
                    "damage_type": {
                        "index": "acid",
                        "name": "Acid",
                        "url": "/api/damage-types/acid"
                    },
                    "damage_dice": "1d8"
                }
            ],
            "actions": []
        },
        {
            "name": "Claw",
            "desc": "Melee Weapon Attack: +11 to hit, reach 5 ft., one target. Hit: 13 (2d6 + 6) slashing damage.",
            "attack_bonus": 11,
            "damage": [
                {
                    "damage_type": {
                        "index": "slashing",
                        "name": "Slashing",
                        "url": "/api/damage-types/slashing"
                    },
                    "damage_dice": "2d6+6"
                }
            ],
            "actions": []
        },
        {
            "name": "Tail",
            "desc": "Melee Weapon Attack: +11 to hit, reach 15 ft., one target. Hit: 15 (2d8 + 6) bludgeoning damage.",
            "attack_bonus": 11,
            "damage": [
                {
                    "damage_type": {
                        "index": "bludgeoning",
                        "name": "Bludgeoning",
                        "url": "/api/damage-types/bludgeoning"
                    },
                    "damage_dice": "2d8+6"
                }
            ],
            "actions": []
        },
        {
            "name": "Frightful Presence",
            "desc": "Each creature of the dragon's choice that is within 120 feet of the dragon and aware of it must succeed on a DC 16 Wisdom saving throw or become frightened for 1 minute. A creature can repeat the saving throw at the end of each of its turns, ending the effect on itself on a success. If a creature's saving throw is successful or the effect ends for it, the creature is immune to the dragon's Frightful Presence for the next 24 hours.",
            "dc": {
                "dc_type": {
                    "index": "wis",
                    "name": "WIS",
                    "url": "/api/ability-scores/wis"
                },
                "dc_value": 16,
                "success_type": "none"
            },
            "actions": []
        },
        {
            "name": "Acid Breath",
            "desc": "The dragon exhales acid in a 60-foot line that is 5 feet wide. Each creature in that line must make a DC 18 Dexterity saving throw, taking 54 (12d8) acid damage on a failed save, or half as much damage on a successful one.",
            "usage": {
                "type": "recharge on roll",
                "dice": "1d6",
                "min_value": 5
            },
            "dc": {
                "dc_type": {
                    "index": "dex",
                    "name": "DEX",
                    "url": "/api/ability-scores/dex"
                },
                "dc_value": 18,
                "success_type": "half"
            },
            "damage": [
                {
                    "damage_type": {
                        "index": "acid",
                        "name": "Acid",
                        "url": "/api/damage-types/acid"
                    },
                    "damage_dice": "12d8"
                }
            ],
            "actions": []
        }
    ],
    "legendary_actions": [
        {
            "name": "Detect",
            "desc": "The dragon makes a Wisdom (Perception) check."
        },
        {
            "name": "Tail Attack",
            "desc": "The dragon makes a tail attack."
        },
        {
            "name": "Wing Attack (Costs 2 Actions)",
            "desc": "The dragon beats its wings. Each creature within 10 ft. of the dragon must succeed on a DC 19 Dexterity saving throw or take 13 (2d6 + 6) bludgeoning damage and be knocked prone. The dragon can then fly up to half its flying speed.",
            "dc": {
                "dc_type": {
                    "index": "dex",
                    "name": "DEX",
                    "url": "/api/ability-scores/dex"
                },
                "dc_value": 19,
                "success_type": "none"
            },
            "damage": [
                {
                    "damage_type": {
                        "index": "bludgeoning",
                        "name": "Bludgeoning",
                        "url": "/api/damage-types/bludgeoning"
                    },
                    "damage_dice": "2d6+6"
                }
            ]
        }
    ],
    "image": "/api/images/monsters/adult-black-dragon.png",
    "url": "/api/monsters/adult-black-dragon"
}

```

- What status code did you get back?

> 200

- Click on the **response** headers in Postman. What are the `Content-Type` and `Content-Length` (provide exact values)?

> `Content-Type` application/json; charset=utf-8

> `Content-Length` 4899

- Summarize the most salient parts of the data you are getting back (for example, Cat facts returns JSON that identifies the source of the cat fact, the cat fact, information about when the fact was created and updated, and the fact itself).

> The summary of the data is that it holds the information about the adult black dragon and its characteristics as well as its abilties.

- How could you use this data in an application?

> I could imagine integrating this API into an app that holds information about DnD creatures and spells for users to look through while playing the game

- What did you like about the documentation?

> The documentation was easy to understand and the main page with the search bar explains how to use it in a simple way

- What did you find challenging about the documentation?

> I found the documentation to be very long and kind of intimidating

- Did the quality of the documentation impact your decision to use it?

> Yes because it looked very professional

- Did you switch which API you chose initially because of its documentation, or did you stick with the one you selected and work your way through it?

> Yes I ended up switching to the DnD one from the Yu-Gi-Oh one because the Yu-Gi-Oh one did not have a search bar

- In your own words, summarize the request-response cycle.

> The request-response cycle is when a client makes a request to the api server and the server grabs the infromation from a database and that information is then sent as a response from the api to the client.

- In your own words, describe what an API is.

> An API is application program interface and is basically a large amount of information about a certain topic that can be used by clients to avoid having to compile all the infromation themselves.

- In your own words, describe the purpose of Postman.

> Postman is an application that makes it easier to interact with an API. With Postman a user can select a http request and receive the information that was asked for.

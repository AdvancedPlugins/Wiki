---
description: Entertain your players endlessly.
---

# 🎮 Chat Games

Chat Games introduce an interactive element to your server's chat, engaging players with challenges like unscrambling words, being the first to type a response, or achieving certain in-game actions. Here's how you can set up a math-based chat game as an example.

## Game Configuration: `games/solve.yml`

{% code title="games/solve.yml" lineNumbers="true" fullWidth="true" %}
```yaml
# Is Chat Game enabled?
enabled: true

# How long should the game last?
length: 15

# Game start routine. This is where you can configure the game start message and requirements.
gameStart:
  effects:
    - 'SET_VARIABLE:math:<random word>8+7,12-5,9*3,16/4,15+6,20-9,7*4,18/3,5+8,14-7,6*5,21/3,11+4,25-10,8*2 </random word>'
    - 'SET_VARIABLE:mathresult:<int><math>%custom_math%</math></int>'
    - "BROADCAST: "
    - "BROADCAST:                               &d&lCHAT GAME"
    - "BROADCAST:       &fThe first person calculate &d%custom_math% &fwill win the game!"
    - "BROADCAST: "

# Game end routine when someone wins. This is where you can configure the game end message and rewards.
gameEndWinner:
  type: ON_MESSAGE
  conditions:
    - "%message% = %custom_mathresult% : %allow%"
  effects:
    - "BROADCAST: "
    - "BROADCAST:                                &d&lCHAT GAME"
    - "BROADCAST: &fThe game has ended! &e%player name% &fwas the first calculate &e%custom_math% = %custom_mathresult%&f!"
    - "BROADCAST: "
    - "CONSOLE_COMMAND:eco give %player name% 250"

# Game end routine when time runs out. This is where you can configure the game end message and rewards.
gameEndNoWinner:
  effects:
    - "BROADCAST: "
    - "BROADCAST:                          &d&lCHAT GAME"
    - "BROADCAST:  &dNo one &fwas able to calculate calculate &d%custom_math% = %custom_mathresult%&f in time!"
    - "BROADCAST:       &fThe game has ended! Better luck next time."
    - "BROADCAST: "
```
{% endcode %}

### Abilities Explanation

[https://wiki.advancedplugins.net/abilities/introduction](https://wiki.advancedplugins.net/abilities/introduction)

### Key Settings Explained

* **enabled**: Activates the chat game feature.
* **length**: Specifies the duration of the game in seconds.
* **gameStart**: Outlines the actions at the start of the game, including setting up the math problem and announcing it to the server.
* **gameEndWinner**: Details what happens when a player wins the game, including conditions for winning and the reward mechanism.
* **gameEndNoWinner**: Defines the outcome if no player solves the game within the time limit, including a message to the server indicating the game has ended without a winner.

### Benefits

* **Engagement**: Chat Games keep the community engaged and active, providing a fun and competitive break from regular gameplay.
* **Learning**: While primarily for fun, these games can also offer educational value, especially with arithmetic challenges.
* **Community Building**: Encourages interaction among players, fostering a sense of community and teamwork.

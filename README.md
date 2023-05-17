# Nim Game

This repository contains the implementation of the Nim Game using Reinforcement Learning (RL). The project was developed as part of the Artificial Intelligence course during my 4th semester.
This is a Python module that implements the Nim game. It includes classes for the game itself, an AI agent for playing against the human, and a gameplay interface.

# Overview
The Nim Game is a classic mathematical game where two players take turns removing objects from distinct piles. The objective is to be the player who removes the last object from the game.

In this project, we utilized RL algorithms to teach an agent to play the Nim Game effectively. By exploring RL policies and understanding their workings, we gained valuable insights into the capabilities of reinforcement learning in learning complex tasks.

# Team Members
1-Ali Raza Github profile link: https://github.com/aliraza998

2-Syed Saadullah Hussaini Github profile link: https://github.com/saadProgram

## Usage

To play the game, run the `main()` function in the `game_of_cards` module.

The game consists of four decks with several cards. The goal is to remove cards from the decks in any order, and the player who makes the last move loses the game.

During the game, you will be prompted to choose the deck and the number of cards to remove. The AI agent will play against you.

# Classes
## Nim
This class represents the Nim game. It has the following methods:

__init__(self, initial: list = [1, 3, 5, 7]): Initializes the game with the specified initial state.
available_actions(cls, piles: list) -> set: Returns the set of available actions in the provided state.
other_player(cls, player: int) -> int: Returns the next player's turn.
switch_player(self) -> None: Switches the turn to the other player.
move(self, action: tuple) -> None: Makes a move in the game.


## NimAI
This class represents an AI agent for playing the Nim game. It uses reinforcement learning to train and improve its performance. It has the following methods:

__init__(self, alpha: float = 0.5, epsilon: float = 0.1): Initializes the AI agent with the specified learning rate and exploration probability.
update(self, old_state: list, action: tuple, new_state: list, reward: int) -> None: Updates the Q values based on the rewards received.
get_q_value(self, state: list, action: tuple) -> float: Returns the Q value for a given state-action pair.
best_future_reward(self, state: list) -> float: Returns the best future reward from a given state.
choose_action(self, state: list, epsilon: bool = True) -> tuple[int, int]: Chooses an action based on exploration or exploitation.


## GamePlay
This class provides a gameplay interface for playing the Nim game. It has the following methods:

progress_bar(cls, progress: int, total: int) -> None: Displays a progress bar.
train(cls, n: int) -> NimAI: Trains the AI agent by playing the game multiple times.
play(cls, ai: NimAI, human: int) -> None: Implements the gameplay where the human and AI take turns playing.
main(loops: int = 10000) -> None: The main function to run the game.

# Usage
Clone the repository: https://github.com/Sameed-75210/Nim-Game-RL.git

# Further Exploration
This project has provided a solid foundation in RL and its application to the Nim Game. Building on this experience, I am enthusiastic about exploring other RL algorithms and their applications in solving real-world problems.

I encourage you to connect with me on LinkedIn to stay updated on my future projects and continue our discussions on artificial intelligence and reinforcement learning.



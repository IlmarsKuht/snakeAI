# snakeAI

This is a deep learning algorithm that learns to play the game snake with the given information about its surrounding environment.

Each state is either true or false

[danger left, danger right, danger straight, direction left, direction right, direction up, direciton down, food left, food up, food right, food down]

In the image below the information would be as follows [0, 0, 0, 0, 0, 1, 0, 1, 0 ,0, 0], direcition is up and food is up, no danger.

It goes through two linear hidden layers and ouputs next state [move left, move right, move straight]

![snake](https://user-images.githubusercontent.com/115834230/199955735-cd24b08f-9020-40da-bc98-528de06ad1c4.png)

Blue lines represent score of each game and orange line the mean of scores.

The algorithm uses Deep Q learning and long short term memory.

Running into itself or the wall means game over and -10 reward, eating an apple is +10 reward.

first 80 games exploration is the main objective of the snake.



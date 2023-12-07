# Dinosaur Game

A simple recreation of [Google Chrome's Dinosaur Game](https://en.wikipedia.org/wiki/Dinosaur_Game) with C, SDL2, and ARMv7 Assembly. 


## Features

### Character Movement

* **Running Animation:** Dinosaur spritesheet leg movement based on running speed.
* **Keyboard Input:** Press the `W` key or the `Spacebar` to make the dinosaur jump. 
* **Gravity:** Dinosaur starts to fall after maximum jump height. The dinosaur can rejump only after it lands.

### Obstacle Movement

* **Random Generation:** Cacti are randomly generated at varied distances.
* **Scroll Speed:** Cacti move at increasingly fast speeds towards the dinosaur.

### Gameloop Termination

* **Collision Detection:** The game terminates if the dinosaur collides with a cactus.
* **Score Calculation:** Scoring is based on the elapsed time before the game terminated.
* **Score Display:** The final score is displayed on the terminal once the game is over.


## Technologies Used

* **C:** Game functionality and logic
* **SDL2:** Graphical interface & keyboard input
* **ARMv7 Assembly:** AABB collision detection


## Getting Started

Follow these steps to set up and run the Dinosaur Game on your **Raspberry Pi**:

### Prerequisites

- [SDL2](https://www.libsdl.org/)

    ```bash
    sudo apt-get install libsdl2-dev
    ```

- [SDL2_image](https://wiki.libsdl.org/SDL2_image/FrontPage)

    ```bash
    sudo apt-get install libsdl2-image-dev
    ```

### Building and Running the Game

1. Clone this repository:

    ```bash
    git clone https://github.com/paulpleela/dinosaur-game.git
    ```

2. Navigate to the project directory:

    ```bash
    cd dinosaur-game
    ```

3. Assemble the Assembly code:

    ```bash
   as -o main.o main.s
    ```  

4. Link libraries and create executable:

    ```bash
    gcc -o dinosaur-game main.o -lSDL2 -lSDL2_image
    ```  

5. Run the game:

    ```bash
    ./dinosaur-game
    ```  


## Contributors

- Myo Pa Pa Kyaw
- Parisorn Prasartkul
- Peeranat Leelawattanapanit
- Phyo Thi Khaing
- Soe Moe Htet


## License

[MIT](https://choosealicense.com/licenses/mit/)
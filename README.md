# 🚀 Alien Invasion (Python Game with MySQL Integration)

This is a classic **2D arcade-style shooter game** developed in Python using **Pygame**. The game is based on the project in _Python Crash Course_ by **Eric Matthes** — but with an upgrade: **MySQL database integration** to store and retrieve high scores! 🏆

  
---

## 🎮 Gameplay


- You control a **spaceship** on the **left side of the screen**.

- Move **up and down** using the `W` and `S` keys.

- Shoot aliens with the `SPACEBAR`.

- Score points by shooting down aliens.

- If you lose all your lives or an alien reaches your ship, the game ends.

- Your score is saved to a **MySQL database**, and the **highest score** is always displayed.

  
---

## 🛠️ Installation

### 1. Clone the repository:

  
```bash

git clone https://github.com/tenoriopedro/AlienGame.git

cd AlienGame

```


### 2. Make the virtual environment and activate it:


```bash

python -m venv venv

.\venv\Scripts\activate.ps1

```

  
### 3. Install dependencies:

  
```bash

pip install -r requirements.txt

```


## 📂 Project Setup Instructions (Important!)
  

Before running the game, follow these **essential steps**:
  

### 1. Create the `.env` file and edit the `CHANGE` values ​​as you wish
  

- In the root of the project, **duplicate** the `.env-example` file and **rename it** to `.env`.


### 2. Using MySQL root.

- Edit the `.env` file and set your MySQL username and password:

```env

DB_USER=your_mysql_user

DB_PASSWORD=your_mysql_password

```

✅ If you're using the default MySQL `root` user, just make sure the password matches the one you used when installing MySQL. If everything is really ok with the `.env` file you can skip step 3.

  

### 3. (Recommended) Create a non-root MySQL user


- If you don’t want to use `root`, follow these steps to create a custom user and grant it privileges:

  
### Open MySQL prompt:

```prompt

mysql -u root -p

```


### Then run these commands one at a time:


- Replace the values ​​below according to your `.env` file
  

```sql

CREATE USER IF NOT EXISTS 'db_user'@'localhost' IDENTIFIED BY 'db_password';

  
GRANT ALL PRIVILEGES ON *.* TO 'db_user'@'localhost';


FLUSH PRIVILEGES;

\q

```


---


## 🧰 Features
  

- 👾 Alien waves increase in difficulty.


- 🔫 Bullet shooting and collision logic.
  

- 🛸 Vertical ship movement from top to bottom (left corner).
  

- 💾 High scores saved in a MySQL database.
  

- 🎓 Clean, modular, object-oriented Python code.


---

  

## Before running the project make shure the `.env` file is configured correctly.


---


## ▶️ How to Play

  
```shell

python main_game.py

```
  

### Controls:
  

- W - Move Up
  

- S - Move Down
  

- SPACE - Shoot
  

---


## 🧠 Based On
  

This game is based on the project in Chapters 12–14 of the book Python Crash Course by Eric Matthes. The MySQL integration is a custom extension.


---  


👨‍💻 Author

Pedro Tenório
  

---


## 📃 License


This project is licensed under the MIT License.

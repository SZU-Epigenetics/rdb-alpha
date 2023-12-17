### Prerequisites

1. [Docker Engine](https://docs.docker.com/engine/)
1. [VS Code](https://code.visualstudio.com/download) and the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
1. Git

### How to Run a Project in Docker

1. Clone the RDB Alpha repo with `git clone https://github.com/SZU-Epigenetics/rdb-alpha.git`
1. Open VSCode, and navigate to the `rdb-alpha` directory.
1. Customize proxy configuration in Dockerfile.
    ```shell
    RUN git config --global http.proxy 'socks5://127.0.0.1:20170'
    RUN git config --global https.proxy 'socks5://127.0.0.1:20170'
    ```
1. Open the terminal and run ``docker build -t freecodecamp:rdb .``
1. Press Ctrl / Cmd + Shift + P and enter `Dev Containers: Reopen in Container`
1. A new VS Code window will open and begin rebuilding the Docker image.
1. Once the image is finished rebuilding, press Ctrl / Cmd + Shift + P and enter `CodeRoad: Start` to open CodeRoad
1. In the CodeRoad window, click "Start New Tutorial"
1. Enter the URL to the `tutorial.json` file of the project you want to start (ex: https://raw.githubusercontent.com/freeCodeCamp/learn-bash-by-building-a-boilerplate/main/tutorial.json)
1. Click the "Start" button

There may be some additional troubleshooting steps to get the container running properly. They can often be solved by following the onscreen instructions, or examining any error messages in your terminal.

### How to Restart or Switch Projects

Note: If you restart or switch projects you will lose your progress, along with any files or directories you created.

1. Press Ctrl / Cmd + Shift + P and enter `Dev Containers: Rebuild Container`
1. Wait for VS Code to reopen and reload the Docker container
1. Open CodeRoad, enter the URL to a `tutorial.json` file, and start the project as described above

### `tutorial.json` File URLs for CodeRoad

- [Learn Bash by Building a Boilerplate](https://raw.githubusercontent.com/freeCodeCamp/learn-bash-by-building-a-boilerplate/main/tutorial.json)
- [Learn Relational Databases by Building a Mario Database](https://raw.githubusercontent.com/freeCodeCamp/learn-relational-databases-by-building-a-mario-database/main/tutorial.json)
- [Celestial Bodies Database](https://raw.githubusercontent.com/freeCodeCamp/learn-celestial-bodies-database/main/tutorial.json)
- [Learn Bash Scripting by Building Five Programs](https://raw.githubusercontent.com/freeCodeCamp/learn-bash-scripting-by-building-five-programs/main/tutorial.json)
- [Learn SQL by Building a Student Database: Part 1](https://raw.githubusercontent.com/freeCodeCamp/learn-sql-by-building-a-student-database-part-1/main/tutorial.json)
- [Learn SQL by Building a Student Database: Part 2](https://raw.githubusercontent.com/freeCodeCamp/learn-sql-by-building-a-student-database-part-2/main/tutorial.json)
- [World Cup Database](https://raw.githubusercontent.com/freeCodeCamp/learn-world-cup-database/main/tutorial.json)
- [Learn Advanced Bash by Building a Kitty Ipsum Translator](https://raw.githubusercontent.com/freeCodeCamp/learn-advanced-bash-by-building-a-kitty-ipsum-translator/main/tutorial.json)
- [Learn Bash and SQL by Building a Bike Rental Shop](https://raw.githubusercontent.com/freeCodeCamp/learn-bash-and-sql-by-building-a-bike-rental-shop/main/tutorial.json)
- [Salon Appointment Scheduler](https://raw.githubusercontent.com/freeCodeCamp/learn-salon-appointment-scheduler/main/tutorial.json)
- [Learn Nano by Building a Castle](https://raw.githubusercontent.com/freeCodeCamp/learn-nano-by-building-a-castle/main/tutorial.json)
- [Learn Git by Building an SQL Reference Object](https://raw.githubusercontent.com/freeCodeCamp/learn-git-by-building-an-sql-reference-object/main/tutorial.json)
- [Periodic Table Database](https://raw.githubusercontent.com/freeCodeCamp/learn-periodic-table-database/main/tutorial.json)
- Learn GitHub by Building a List of Inspirational Quotes (in progress)
- [Number Guessing Game](https://raw.githubusercontent.com/freeCodeCamp/learn-number-guessing-game/main/tutorial.json)


### What has changed compared to the original version
1. Building the Docker image manually.
1. Set up a proxy for Git.
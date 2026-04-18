# CodeQuest 23 Python Tank Bot
Controls a tank in the CodeQuest 2023 Hackathon game. For more information about the hackathon see https://codequest.club


## Running the bot
The bot can be built as a Docker image using the included Dockerfile.
```docker build -t tankTrouble .```
The image can then be run as a container.
```docker run tankTrouble```


## Changing the Dockerfile
There are a few requirements for the Docker image:
- The final image should have a file at `/codequest/run.sh`. Whatever this file prints will be taken as the bot's output and will be sent to the game server.
Do not print logs or run other commands in this file. It should only run the bot e.g. `python src/main.py`.
Any dependencies that need to be installed should be done somewhere else in the Dockerfile.
- The final image needs to be Linux based. It also needs to have Python (>=3.9) and `socat` installed. These are
already provided in the Dockerfile in this repo.

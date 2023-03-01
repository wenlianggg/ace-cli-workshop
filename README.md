# ACE Command Line Fundamentals (Lab)
Introductory command line workshop, presented by the SCIS ACE Programme.

## Creating your own Lab environment
_Pre-requisites: Docker and Git installed on your computer_

1. Clone this git repository to download the code
```bash
git clone https://github.com/wenlianggg/ace-cli-workshop 
```

2. Change your directory into the repository with the code
```bash
cd ace-cli-workshop
```

3. Run Docker Compose to build and run this Docker image. \
Please bear in mind that this step might take up to **10 minutes** depending on the speed of your computer and internet bandwidth.
If `docker compose` does not work on your computer, try `docker-compose`
```bash
docker compose -f docker-compose.personal.yml build
```

4. Start the Docker containers.
```bash
docker compose -f docker-compose.personal.yml up -d
```

5. You should now be able to SSH into your own container. Please note that only ports 3201 and 3202 are made available in the `docker-compose.personal.yml` as it is meant for your use only.
```bash
ssh workshop@localhost -p 3201
```
When prompted, provide the password `aceCLI!`

If you're curious about how the lab environment is set up with Docker, please check out the contents of `Dockerfile` to see how the image is created.

## Windows Users: Beyond the Lab Environment
Mac OS is a Unix-based operating system, and naturally has shell capabilities similar to the Ubuntu lab environment provided.

For Windows users, you will need to perform additional steps to run Linux on your machine through the Windows Subsystem for Linux (WSL).

You may read the [Microsoft Guide on Installing WSL](https://learn.microsoft.com/en-us/windows/wsl/install) for more information.

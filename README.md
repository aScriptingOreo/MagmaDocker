# Magma Docker
This project allows quick deployment of a Minecraft Server(version 1.12.2) distro named Magma on Docker

-	Docker allows for a faster and easier deployment of the server, allowing it to be cross-platform compatible
-	Magma allows for more flexibility due to it's capability to bridge Spigot(paper in this case) and Forge, granting us the ability to install ForgeMods and/or Bukkit/Spigot Plugins.


## Installation
 1. Clone this Repository:
	- `git clone https://github.com/aScriptingOreo/MagmaDocker`
 2. Install Docker
	- Docker Desktop (Windows only):
		-  `https://www.docker.com/products/docker-desktop`
	- Docker CLI (Linux):
		- `https://docs.docker.com/engine/install/ubuntu/`
3. Stack Configuration
	- Edit `.env`(located inside the `/MagmaDocker/` folder) with your desired Text editor/IDE (Notepad++, VSCode, ItelliJ, etc) and locate the variables:
		- ``WEBRCON_USER`` - This is the Login for the Remote Console web app.
		- ``WEBRCON_PASS`` - This is the Password for the Remote Console web app.
	- Change them to whatever you desire. 
	- **Please keep in mind the formatting while changing the `.env` file, always write inside `""` quotation marks**.
5. Build the Stack
	-	On the folder `/MagmaDocker/` open your terminal of choice and run the following command:
		-	`docker-compose --env-file .env -f ./stack.yml  up -d`

6. Server Configuration
	-	The your Minecraft Server files should be in the `/MagmaDocker/Magma_Server/` folder, in order to apply any file changes to your server [restart the container through docker](https://docs.docker.com/engine/reference/commandline/restart/).

7. Server interfacing
	- This stack uses the amazing [ITZG Rcon Web Admin panel](https://github.com/itzg/docker-rcon-web-admin) to give you direct access to your server's console without headaches, by default, the stack should host this on [localhost:4326](http://localhost:4326) (If you're not hositng the stack on your local machine, use ``http://"TargetIP/DNS":4326`` (be sure firewall rules are allowing access to the ports).
	- Log in with the credentials you've set up on step 3.


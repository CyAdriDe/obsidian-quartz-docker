# obsidian-quartz-docker

Remote desktop for obsidian usage with docker, also being able to publish in another docker using quartz.

First, check the ports that you want to open for the dockers in both docker-compose files. Also create a folder with your vault name in the wiki folder.

You need to first do:

```
docker-compose -f obsidian.docker-compose.yml up -d
```

This will start the obsidian docker. This is an rdp to a web server, meaning that only one person at a time can use it.

Then, you can start the quartz docker:

```
docker-compose -f wiki.docker-compose.yml up -d
```

This will start the wiki page and updated everytime there is a change in the obsidian vault. For version control it will be interesting to put a git plugin.

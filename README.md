# openjdk-workshop

## getting started using docker

- clone the repos, notice the target location and the symlink, if you change one, you need to change the other

The symlink is there to help resolve IDE configurations, which we will cover in [Task 0](#task-0--ide-setup)

```bash
git clone https://github.com/viqueen/jdk.git --depth 1 --no-tags ~/workshop-sources/jdk
git clone https://github.com/viqueen/openjdk-workshop.git ~/workshop-sources/openjdk-workshop

ln -sfnv ~/workshop-sources /tmp/workshop-sources
```

- compose them up

```bash
cd ~/workshop-sources/openjdk-workshop
docker compose up -d
```

- open terminal session

```bash
docker exec -it openjdk-workshop-session-1 bash
```

## task 0 : IDE Setup

- in the container terminal session

```bash
cd /tmp/workshop-sources/jdk
bash configure
```

- if you are using IntelliJ IDEA
```bash
bash bin/idea.sh
```

- if you are using VSCode run the command and then open `build/linux-x86_64-server-release/jdk.code-workspace` file in VSCode
```bash
make vscode-project
```
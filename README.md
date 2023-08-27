## openjdk-workshop

### requirements

- git
- Java 20 , I recommend using SDKMAN for this

### get the code

<details>
<summary>using docker</summary>
<p>

- clone the repos, notice the target location, this is mapped volume on our docker compose

The symlink is there to help resolve IDE configurations

```bash
git clone https://github.com/viqueen/jdk.git --depth 1 --no-tags /tmp/sources/jdk
git clone https://github.com/viqueen/jtreg.git --depth 1 --no-tags /tmp/sources/jtreg
git clone https://github.com/viqueen/openjdk-workshop.git /tmp/sources/openjdk-workshop
```

- compose them up

```bash
cd /tmp/sources/openjdk-workshop
docker compose up -d
```

- open terminal session

```bash
docker exec -it openjdk-workshop-session-1 bash
```

</p>
</details>

<details>
<summary>using local environment</summary>

- clone the repos

```bash
git clone https://github.com/viqueen/jdk.git --depth 1 --no-tags /tmp/sources/jdk
git clone https://github.com/viqueen/jtreg.git --depth 1 --no-tags /tmp/sources/jtreg
git clone https://github.com/viqueen/openjdk-workshop.git /tmp/sources/openjdk-workshop
```

</details>
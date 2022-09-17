# To Do 

* deploy on vps DONE
  access the postgres databse using docker 

  ```bash
  docker exec -it pgdb_build_it_2022 bash
  ```
  after insert into the service of pgdb_build_it_2022 container we can run 

  ```bash
  psql --host=pgdb_build_it_2022 --dbname=build_it_2022_practice --username=build_it
  ```
  then just type the password, to access the sqlpad we can just go to [sqlpad](http://103.186.1.168:3001/signin)

* testing DONE 
* create the user login DONE
* setup database for the practice ON PROGRESS

# How to deploy

The deployment u can use any VPS with [docker](https://docs.docker.com/engine/install/) installed.

For Details use the step below

1. You can ssh to your VPS then install the docker I recommend a VPS using linux based OS such as ubuntu or debian. 

```bash
ssh <username>@<hostname>
```

2. After ssh to your VPS you can make sure that git is installed using

```bash
git -v
```

3. If git is not installed then u can do 

```bash
sudo apt install git
```

If you are using centOS then you can use `yum` instead of `apt`

3. Install docker

Click for each OS :

* [CentOS]( https://docs.docker.com/engine/install/centos/ )
* [Debian ]( https://docs.docker.com/engine/install/debian/ )
* [Ubuntu]( https://docs.docker.com/engine/install/ubuntu/ )
* [Arch  ]( https://wiki.archlinux.org/title/Docker )

Don't Forget to install [Docker Compose](  https://docs.docker.com/compose/install/  )

4. Clone this Repo 

clone the repo into your VPS 

```
git clone https://github.com/gricowijaya/postgres-build-it-2022-service.git
```

5. Edit the environment variables

Copy the `.env.example` file by using command :

```bash
cp .env.example .env
```

6. Up the service 

Compose the service of psql and sqlpad.

```
docker compose up -d
```

7. Access the SQLpad.


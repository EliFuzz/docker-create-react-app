<h1 align="center">Docker Compose create-react-app boilerplate</h1>
<p align="center">This is a Docker Compose boilerplate for NodeJS with `yarn, create-react-app`, based on Alpine Linux image</p>
<p align="center">
  <img width="150" height="150" src="https://raw.githubusercontent.com/docker/compose/master/logo.png" alt="Docker compose logo">&nbsp;
  <img width="200" height="150" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png" alt="React logo">&nbsp;
</p>

---

## Into:
This docker Node.js boilerplate is a wrapper of [docker hub image](https://hub.docker.com/_/node/) with pre-installed `yarn, create-react-app`.

## Installation:
1. Clone repository:
<pre class="command-line">
    <span class="command">git clone https://github.com/EliFuzz/docker-create-react-app.git</span>
</pre>
2. Go to folder:
<pre class="command-line">
    <span class="command">cd docker-create-react-app</span>
</pre>
3. Copy and rename `.env_bak` to `.env`:
<pre class="command-line">
    <span class="command">cp .env_bak .env</span>
</pre>
4. Build docker:
<pre class="command-line">
    <span class="command">docker-compose up -d</span>
</pre>
5. Init react app (only once):
<pre class="command-line">
    <span class="command">docker-compose exec dev sh -c "create-react-app app"</span>
</pre>
6. Run NPM start script:
<pre class="command-line">
    <span class="command">docker-compose exec dev sh -c "yarn start"</span>
</pre>
7. Open browser: [localhost:3000](http://localhost:3000/)
8. Exit docker:
<pre class="command-line">
    <span class="command">docker-compose down</span>
</pre>


## Settings:
`.env`:
- NODE_PORT=**3000**
- NODE_ENV=**development**

`docker/dev/Dockerfile`:
- FROM node:**10.9.0-alpine** - you can change node version. Look for reference: [Docker Hub](https://hub.docker.com/_/node/)

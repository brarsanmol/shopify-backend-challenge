# spotify-backend-challenge

## Sections
  - [Usage With Docker](#usage-with-docker)
  - [Usage Without Docker](#usage-without-docker)

## Usage With Docker
- Clone The Repository With Submodules
   - `git clone --recurse-submodules --remote-submodules https://github.com/brarsanmol/shopify-backend-challenge.git`
- Ensure That You Have Docker, If You Don't Install and Setup [Docker Desktop](https://www.docker.com/get-started).
- `cd` Into The `client` Directory And Create A `.env` File. (I recommend the configuration below.)
```
# Frontend Address
REACT_APP_BASE_URL=http://localhost:4000

# Backend Address
REACT_APP_SERVER_ADDRESS = http://localhost:3000
```
- `cd` Into The `server` Directory And Create A `.env.production` File. (I recommend the configuration below.)
```
# Backend Port
PORT=3000

# Frontend Address
CLIENT_ADDRESS=http://localhost:4000

# Used By TypeORM for Database Credentials
TYPEORM_CONNECTION=postgres
TYPEORM_SYNCHRONIZE=true
TYPEORM_DATABASE=shopify
TYPEORM_HOST=database
TYPEORM_PORT=5432
TYPEORM_USERNAME=postgres
TYPEORM_PASSWORD=shopify
# TYPEORM_LOGGING=true
TYPEORM_ENTITIES=build/entities/*.js,src/**/entities/*.ts

# Used By Docker For Database Credentials.
POSTGRES_DB=shopify
POSTGRES_USERNAME=postgres
POSTGRES_PASSWORD=shopify
```
- `cd` Back Into The Main `shopify-backend-challenge` Directory.
- Run `docker-compose up --build`
- For The Final Step, If You Have Followed The Default Configuration Now Open Your Browser And Type `http://localhost:4000`. If You Have Not Followed The Default Configuration Adjust The Port Accordingly.

## Usage Without Docker
- Clone The Repository With Submodules
   - `git clone --recurse-submodules --remote-submodules https://github.com/brarsanmol/shopify-backend-challenge.git`
- Ensure That You Have [Node.js](https://nodejs.org/en/) Installed On Your Machine.
- Ensure That You Have [PostgresSQL](https://www.postgresql.org/download/) Installed On Your Machine.
- `cd` Into The `client` Directory And Run `npm install`.
- Create A `.env` File In The Client Directory. (I recommend the configuration below.)
```
REACT_APP_BASE_URL=http://localhost:3000

REACT_APP_SERVER_ADDRESS=http://localhost:4000
```
- `cd` Into The `server` Directory And Run `npm install`.
- Create A File Called `.env.production` In The Server Folder And Paste The Following In.
- Ensure That You Have The User With The Name `shopify` Created And A Database Named `shopify` Created In PostgreSQL If You Choose To Go With The Default Settings.
```
# Backend Address
PORT=4000

# Frontend Address
CLIENT_ADDRESS=http://localhost:3000

# Used By TypeORM for Database Credentials
TYPEORM_CONNECTION=postgres
TYPEORM_SYNCHRONIZE=true
TYPEORM_DATABASE=shopify
TYPEORM_HOST=database
TYPEORM_PORT=5432
TYPEORM_USERNAME=postgres
TYPEORM_PASSWORD=shopify
# TYPEORM_LOGGING=true
TYPEORM_ENTITIES=build/entities/*.js,src/**/entities/*.ts
```
- In Your Terminal `cd` Into The `server` Directory And Run `npm run develop`.
- In Your Terminal (Open Another Instance) `cd` Into The `client` Directory And Run `npm start`.
- For The Final Step, If You Have Followed The Default Configuration Now Open Your Browser And Type `http://localhost:3000`. If You Have Not Followed The Default Configuration Adjust The Port Accordingly.
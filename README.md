# spotify-backend-challenge

## Usage
- Clone The Repository With Submodules
   - `git clone --recurse-submodules --remote-submodules`
- Ensure you have [Node.js](https://nodejs.org/en/) installed on your machine.
- `cd` into both the client and server folder and run `npm install`
- Ensure that you have [PostgresSQL](https://www.postgresql.org/download/) installed on your machine.
- Create a file called `.env.development` in the server folder and paste the following in. 

```PORT = 4000 # Server Port
CLIENT_ADDRESS = http://localhost:3000 # Frontend Address

TYPEORM_CONNECTION = postgres
TYPEORM_HOST = localhost
TYPEORM_PORT = 5432
TYPEORM_USERNAME = shopify
TYPEORM_PASSWORD =
TYPEORM_DATABASE = shopify-challenge-development
TYPEORM_SYNCHRONIZE = true
# TYPEORM_LOGGING = true
TYPEORM_ENTITIES = build/entities/*.js,src/**/entities/*.ts
```

- Create a file called `.env` in the client folder and paste the following in.
```
REACT_APP_BASE_URL = http://localhost:3000

REACT_APP_SERVER_ADDRESS = http://localhost:4000
```

- In your terminal `cd` into the server folder and run `npm run develop`.
- In your terminal `cd` into the client folder and run `npm start`.

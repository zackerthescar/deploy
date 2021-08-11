# gitea-drone

Deploy Gitea with Postgres DB, Drone CI

Based on [@Anne](https://github.com/1byte2bytes)'s [Gitea-Drone](https://code.boonchuy.nl/anne/deploy/-/tree/master/Gitea-Drone)'s files, with the inclusion of an `.env` file to make configuring the deployment easier.

This docker-compose file is ridiculously easy to use, just edit the `.env` and `env_vars` files, follow a simple guide to allow Drone logins via Gitea, and done!
#

**.env**
Variables to change for your instance
|Variable|Description  |
|--|--|
|**DOMAIN**  | The domain you wish to deploy gitea and drone to |
| **NETWORK** | The network that your reverse proxy container is attached to
| **APP_NAME** | The name of your Gitea instance
#

**env_vars**
Variables regarding Drone CI
| Variable | Description |
|--|--|
| DRONE_RPC_SECRET | Add a random string. This is used as a secret string between the Drone runner and agent containers |
 | DRONE_GITA_CLIENT_ID | After configuring and setting up the first Gitea account, follow [this guide](https://docs.drone.io/server/provider/gitea/#create-an-oauth-application) to let Drone login via Gitea
 | DRONE_GITEA_CLIENT_SECRET | After configuring and setting up the first Gitea account, follow [this guide](https://docs.drone.io/server/provider/gitea/#create-an-oauth-application) to let Drone login via Gitea|
#
**Credits:**

[@Anne](https://github.com/1byte2bytes): her [Gitea-Drone](https://code.boonchuy.nl/anne/deploy/-/tree/master/Gitea-Drone) configuration on which mine is heavily based on.





# Prerequisites

Verify that you have and can do all these steps

- Non-CGNAT IP address (static/dynamic)
- Ability to Port Forward
- MongoDB Server
- Node.js >14.0.0
- A subdomain so you can do HTTPS

# How to install

- Go on taku and click the hammer button under the + button
- Enter a name for your guild in the input field
- Save the `AUTH_KEY` the website will give you,
  it looks something like this:
  `taku.zLEöIks123EaΣXQ!ravCEEi0FA#.dW8NπjH4xdUf8kHG#eFqO3G1khX.gncm`
- Clone the [taku.server](https://github.com/taku-moe/taku.server) repository
- Make sure your MongoDB server is running
- Run `npm i` to install the dependancies
- Run `npm run prod` to startup the server for the first time
- The server will terminate and generate a `settings.json`, edit it to your config
- Here is an example config: 
  ```js
  {
    // The interface you want the server to bind to
    "ip": "", 
    // The URL to your mongodb (it can be left as default 
    // if the database is hosted on the same machine)
    "database_url": "mongodb://localhost:27017/taku",
    // The port you want the server to run on
    "port": 9669,
    // This is the enduser hostname clients will use to access your server
    "hostname": "https://taku.geoxor.moe:9669",
    // If whitelisting is enabled so random users can't join
    "is_whitelisted": false,
    // This is unused so don't worry about it
    "use_internal_db": true,
    // This is your AUTH_KEY that you will get from taku.moe
    // when creating a new guild
    "auth_key": "<YOUR_AUTH_KEY>"
  }
  ```
- Run `npm run prod` again to startup your guild
- If no errors happen then you should see your guild online on [taku.moe](https://taku.moe) otherwise please report the errors on the server issues [taku.server Issues](https://github.com/taku-moe/taku.server/issues)
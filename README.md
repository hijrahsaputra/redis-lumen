# redis-lumen
project app redis and lumen 

<!-- GETTING STARTED -->
### Prerequisites

Install and config Redis on Mac OS X via Homebrew

By using Homebrew, you greatly reduce the cost of setting up and configuring the development environment on Mac OS X.

Let’s install Redis for the good.
```sh
  $ brew install redis
  ```
After installation, you will see some notification about some caveats on configuring. Just leave it and continue to following some tasks on this article.

Launch Redis on computer starts.
```sh
$ ln -sfv /usr/local/opt/redis/*.plist ~/Library/LaunchAgents
```
Start Redis server via “launchctl”.
```sh
$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.redis.plist
```
Start Redis server using configuration file.
```sh
$ redis-server /usr/local/etc/redis.conf
```
Stop Redis on autostart on computer start.
```sh
$ launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.redis.plist
```
Location of Redis configuration file.
```sh
/usr/local/etc/redis.conf
```
Uninstall Redis and its files.
```sh
$ brew uninstall redis
$ rm ~/Library/LaunchAgents/homebrew.mxcl.redis.plist
```
Get Redis package information.
```sh
$ brew info redis
```
Test if Redis server is running.
```sh
$ redis-cli ping
```
If it replies “PONG”, then it’s good to go!
Well, I guess, that’s it!
Have fun Redis-ing ☺

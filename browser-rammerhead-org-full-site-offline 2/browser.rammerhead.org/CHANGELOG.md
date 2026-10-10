# Current version

## v1.2.1 (beta)

- built on rammerhead v1.3.1 (beta)
- cloudflare's "verify you are human" checks pass without the checkbox (no speed ticket needed)
- fix discord.com
- fix youtube and spotify scripts being blocked by their own security policies
- fix memory leak: websocket connections to sites never closing (tiktok, spotify, twitch)
- fix memory leak: blocklist dns lookups never timing out
- fix pages hanging under load (mostly tiktok)
- fix server crashes (malformed cookies, odd hostnames and headers, blocked websockets)
- fix many sites' dynamically added scripts not being proxied in newer chrome
- fix cloudflare challenges for sites serving zstd, and the challenge page reloading itself
- faster, cheaper cloudflare solving for speed ticket users: one paid solve per site instead of two, reused by every session and worker, and no more hanging after another user solved it
- speed ticket users only fall back to the cloudflare solver when cloudflare's own check fails, with a message while it solves
- the "you need a speed ticket" message only shows when cloudflare's own check fails, and no longer covers the checkbox
- move secrets out of docker-compose.yml defaults into each server's .env
- rotate docker container logs
- faster under load (about half the cpu per request)
- use duckduckgo for search and suggestions (google always shows a captcha)
- docker images use node 26

&nbsp;

# Previous versions #

## v1.1.6

- fixed slightly updated cloudflare challenge for speed ticket users

&nbsp;

## v1.1.5

- removed deprecated Alienhub
- added speed ticket panel
- added general adblock, youtube adblock, and vpn locations for speed ticket users
- fixed and removed ads and the anti-adblocker message for now.gg (no speed ticket needed)
- fixed Geforce Now login

&nbsp;

## v1.1.4

- migrating to new domain system
- add Alienhub Basic residential proxy support
- allocate dedicated speed to Alienhub Basic users
- optimized initial page load ("Connecting to server..." is much faster now)
- added `javascript:` support
- added bash.gg ad

## v1.1.31

- fix "Enable URL Shuffling" in rh://settings not working the first time you click
- fix random 502 errors

## v1.1.3

- added load balancing!! things are much faster now (thank you Alienhub for providing the server. please go check them out, they are very cool)
- fix Alienhub signup page

## v1.1.2

- add support for mac users for command-click key opening full url
- faster real-time streaming

## v1.1.1

- add sponsor link

## v1.1.0

- change rammerhead protocol from `rammerhead://` to `rh://`
- add long overdue new tab button
- add long overdue feature of importing and exporting browser profiles
- add long overdue message when initial connection fails
- add globe image for sites without a favicon
- add reset button in `rh://settings`
- add option to change tab title and favicon
- design changes here and there
- update `rh://welcome` for new import/export feature
- fix bug of localStorage saving not working (logins like discord should stick now)
- reshuffle urls with every new session
- reorganize changelog format

## v1.0.4

- add file cache support from rammerhead update
- temporarily switch back to nodejs cluster system as load times should be much much faster

## v1.0.3

- switch scaling method from nodejs cluster to kubernetes system
- remove Arc.io

## v1.0.23

- update localStorage key references to new rammerhead custom localStorage implementation

## v1.0.22

- fix Arc.io service worker

## v1.0.21

- prevent URL from lowercasing when entered in browser (urls entered with caps works now)
- add browser-bar URL recognition support for IPv4 addresses
- experimentally add Arc.io as a test for a possible source of server funding

## v1.0.2

- add server multithreading support

## v1.0.12

- fix localStorage `rhdatabase` cleanup

## v1.0.11

- switch to use `localStorage` instead of `sessionStorage` for keeping track of cleanups

## v1.0.1

- add version number to new tab page
- add `rammerhead://changelog`
- add url suggestions for rammerhead:// urls
- add similar UI of old rammerhead to new tab page

## v1.0.0

- Rammerhead browser release

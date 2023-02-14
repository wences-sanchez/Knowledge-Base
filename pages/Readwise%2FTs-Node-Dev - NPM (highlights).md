title:: Readwise/Ts-Node-Dev - NPM (highlights)
deck:: [[Across-the-Net]]
author:: [[chokidar]]
full-title:: "Ts-Node-Dev - NPM"
category:: #articles
url:: https://www.npmjs.com/package/ts-node-dev

- Highlights first synced by [[Readwise]] [[Tuesday, 14-02-2023]]
	- -
		- ts-node-dev
		  
		  > Tweaked version of [node-dev](https://github.com/fgnass/node-dev) that uses [ts-node](https://github.com/TypeStrong/ts-node) under the hood.
		  
		  It restarts target node process when any of required files changes (as standard `node-dev`) but shares [Typescript](https://github.com/Microsoft/TypeScript/) compilation process between restarts. This significantly increases speed of restarting comparing to `node-dev -r ts-node/register ...`, `nodemon -x ts-node ...` variations because there is no need to instantiate `ts-node` compilation each time. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gs874navemp4y9jyvs1r5tys))
	- -
# Openshift Labs Node.JS

## Usage

1. **Create an app from LTS 4** `rhc create-app <app name> http://nodecartridge-dongrht.rhcloud.com/manifest/LTS-4`
1. **Create an app from LTS 6** `rhc create-app <app name> http://nodecartridge-dongrht.rhcloud.com/manifest/LTS-6`
2. **Create an app from the latest stable release** `rhc create-app <app name> http://nodecartridge-dongrht.rhcloud.com/manifest/stable`
3. **Create an app from the latest unstable release** `rhc create-app <app name> http://nodecartridge-dongrht.rhcloud.com/manifest/unstable`

What this cartridge provides out of the box
---
1. **node.js** ([latest LTS](https://semver.io/node/resolve/6) currently 6.9.1)
2. **npm** (latest stable currently 3.10.8)
3. **grunt**
4. **bower**

What this cartridge does out of the box
---
*Not much.*

1. Installs node.js (version specified by `$OPENSHIFT_NODEJS_VERSION` and resolved by [semver.io](https://semver.io))
2. Installs grunt, bower, and forever globally (specified by `$OPENSHIFT_NPM_GLOBALS`)
3. Allows the user to manually install required dependencies (in a `build` [action_hook](http://openshift.github.io/documentation/oo_user_guide.html#action-hooks))
4. Runs `npm start` if `package.json` is found in repo directory (log is written to `$OPENSHIFT_NODEJS_LOG_DIR`)

Thanks to all!
---
These repos helped out a ton while developing this cartridge.

1. [connyay/openshift-node-diy](https://github.com/connyay/openshift-node-diy)
2. [smarterclayton/openshift-cdk-cart](https://github.com/smarterclayton/openshift-cdk-cart)

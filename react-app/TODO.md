- moving all configurations to package file
- not to edit .aio file or add config there
- keeping the uiBuild, uiDev and dist folder locations separate



TODO
- fix the check for web-src and allow build to run without index.html

## Local Development

1. Single command window
- Have frontend code in a directory under ff app
- config .aio file to add
  - web - the path to the frontend directory
  - runScript - Package script to run frontend locally
- run `aio app run` to run the ui locally


2. Run frontend build as a separate process
- Have frontend code in a directory under ff app
- config .aio file to add
  - web - the path to the frontend directory
- run the custom frontend build/dev in a separate window (npm start)
- run `aio app run --skip-build` to run the ff app locally without frontend (parcel) build
- this would still create the config.json file inside `<cna.web>/src/config.json`


3. Running frontend script using aio-run-detached
- Have frontend code in a directory under ff app
- Install `aio-run-detached` as a dev dependency
- add a custom dev script which runs the dev command using `aio-run-detached`
  - `"start:detached": "aio-run-detached react-scripts start"`


## Building and deploying



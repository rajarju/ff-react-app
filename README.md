# Create React APP + FF

## Setting up
1. Generate a new app ~~with Vanilla template~~
2. Replace web-src with existing create react app
   1. Add exc-runtime to the existing react project if needed
3. Create index.html file under web-src to fool the `aio app run` to generate `config.json`.

## Local development
1. Run `aio app run [--local]` to start the FF app
   1. This will generate the `config.json` file
2. Run React UI separately `HTTPS=true npm start`
3. Replace port on ECX test page

## Building and deploying 
1. Build dev/prod UI with custom script
2. Deploy with cli `aio app deploy --skip-build`
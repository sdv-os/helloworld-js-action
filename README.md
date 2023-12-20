# Hello world javascript action

This action prints "Hello World" or "Hello" + the name of a person to greet to the log.

## Inputs

### `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

### `time`

The time we greeted you.

## Example usage

```yaml
uses: sdv-os/helloworld-js-action@main
with:
  who-to-greet: 'Aric Demo'
```

## Edit Code
npm install @actions/core
npm install @actions/github
Programming and test this step.

## Compile the scripts.


Install vercel/ncc by running this command in your terminal.

npm i -g @vercel/ncc

Compile your index.js file.

ncc build index.js --license licenses.txt

You'll see a new dist/index.js file with your code and the compiled modules. You will also see an accompanying dist/licenses.txt file containing all the licenses of the node_modules you are using.

Change the main keyword in your action.yml file to use the new dist/index.js file.

main: 'dist/index.js'

If you already checked in your node_modules directory, remove it.

rm -rf node_modules/*

From your terminal, commit the updates to your action.yml, dist/index.js, and node_modules files.

# Tutorial extension for Theia and VSCode

The tutorial extension is displaying a tutorial based on a .json file. One tutorial can have multiple exercise-steps. Each exercise can display different content types but also can execute commands in the terminal, add imports and run checks on the progress of the learner. All of that has to be defined in the .json file inside the workspace.

## Feedback, Help and Support

Feel free to start a discussion by opening an issue on this repo or by contacting us [directly via email](mailto:info@eclipsesource.com).

## Developers Documentation

### First time setup

- Install [node.js](https://nodejs.org/) (version >= 6.x.x)
- Update npm (version >= 5.8.0)
- Clone this repository
- Install dependencies: `yarn install`

### Build & Testing

```
yarn compile
```

After that press `F5` to run the application.

### Packaging and Publishing

#### Packaging

```
npm install -g vsce
vsce package
```

#### Publishing

Under [open-vsx.org](https://open-vsx.org/) register with your GitHub account and generate an Access Token.

```
npx ovsx create-namespace <name> -p <token>
npx ovsx publish <file> -p <token>
```

Where **name** is the extension's `publisher` field in the package.json file and **file** is the path to the .vsix file generated in the first step.

A detailed description of publishing to Open VSX can be found [here](https://github.com/eclipse/openvsx/wiki/Publishing-Extensions).

Instructions to publish the extension on the Visual Studio Marketplace can be found [here](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)

## License

- [Eclipse Public License 2.0](https://opensource.org/licenses/EPL-2.0)
- [The MIT License](https://opensource.org/licenses/MIT)

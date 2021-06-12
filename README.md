# ezpp! experimental

ezpp! experimental is a fork of ezpp! and a browser extension that allows you to calculate pp
values for a beatmap without manually downloading the beatmap.

[changelog](https://next.acrylicstyle.xyz/ezpp.html#ezpp_experimental)

Feel free to ask in [discussion](https://github.com/acrylic-style/ezpp/discussions) if you have any questions!

Please note that experimental branch will not be merged into ezpp!. A new branch will be created for a new feature and will be PR'd from that branch.

## Features (specific to experimental)
- Full taiko star rating/pp calculation (aka Full taiko support)
- Fix original metadata display if unicode title/artist is missing
- Fix AR calculation with HT+HR (with simpler code)
- Fix some part of an artist is missing on some beatmap
- [\[Proposal\] Collapsible pp details design](https://github.com/oamaok/ezpp/pull/119)
- Change header color depending on the star rating
- Make it work on score details page
  - With auto-fills.
- Fix throwing error on discussion page
  - Extension popup will be hidden (you cannot open) on discussion page.
- Add Bulgarian Translation
- Update German Translation
- Update Chinese Translation
- Add Croatian Translation

## Supported modes

PRs are welcome for unsupported modes. (See `Contributing > Pull requests` below)

Full support
- osu!
- osu!taiko

Partial support

Unsupported
- osu!catch
- osu!mania


## Contributing

### Issues

If you are reporting issue that also exists in ezpp! (not experimental): Please report on [oamaok/ezpp](https://github.com/oamaok/ezpp/issues).

If you are reporting issue that does not exist in ezpp! and specific to experimental: Please report on [this repository](https://github.com/acrylic-style/ezpp/issues).

All feature requests should be created at [oamaok/ezpp](https://github.com/oamaok/ezpp/issues) unless you're creating a feature request (that improves the existing feature) to the feature that already exists in this repository.

### Pull requests

All contributions to ezpp! are warmly welcome, but you should not PR on this repository if your fixes are not specific to experimental branch. (you MUST create a PR on this repository if your fix applies only for ezpp! experimental). Please create a PR on [oamaok/ezpp](https://github.com/oamaok/ezpp) and I will update the experimental branch too.

## Developing

### Prerequisities

Versions of software used at the time of writing:

```shell
[teemu@home ezpp]$ node -v
v14.15.4
[teemu@home ezpp]$ yarn -v
1.22.4
```

### Setup

Clone the repository and run the following commands.
```
yarn
```

### Chromium-based browsers

 - Run `yarn start:chrome`. This will create a `build/` directory to the repository root.
 - Open up Chrome and navigate to `chrome://extensions`.
 - Enable `Developer mode`.
 - Click the `Load unpacked` button and select the previously mentioned `build` directory. 
 - The extension is now ready to go!

All the changes made are compiled automatically as long as the `yarn start:chrome` script is running.

To build a production version of the package, run `yarn build:chrome`.

### Firefox

 - Run `yarn start:firefox`. This will create a `build/` directory to the repository root.
 - Open up Firefox and navigate to `about:debugging#/runtime/this-firefox`.
 - Click the `Load Temporary Add-on` button and select any file in the previously mentioned directory.
 - The extension is now ready to go!

All the changes made are compiled automatically as long as the `yarn start:firefox` script is running.

To build a production version of the package, run `yarn build:firefox`.

### Production builds

Run `yarn build:all`. Two files, `ezpp-chrome.zip` and `ezpp-firefox.zip`, are generated.

## Installing

Chrome/Chromium: [Install from Google WebStore](https://chrome.google.com/webstore/detail/iihpkkdlbfcanaaignnjcgmlhhbpoioh)

<!-- I didn't publish on AMO -->
<!--Firefox: [Install from addons.mozilla.org](https://addons.mozilla.org/en-US/firefox/addon/ezpp/)-->

## License

[MIT](https://github.com/oamaok/ezpp/blob/master/LICENSE)

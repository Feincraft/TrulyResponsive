# Truly Responsive
## About
**Truly Responsive** is a framework to build PowerApps that present different UXs, based on the device they are running on. This in contast to "stretchy designs" where UI elements just stretch to fill in avaialble space.

Included in the package are a demo app and The Watcher, a reusable component that enables Makers to create their own Truly Responsive designs.

Watch the video: https://www.youtube.com/watch?v=SsYOt-ITVZs

## Demo App
The app has 4 UXs, covering: Phones, Portrait Tablets, Landscape Tablets and Desktops.

![](https://github.com/Feincraft/TrulyResponsive/blob/main/TrulyResponsive%20O110.gif?raw=true)

All UX elements are real and there's data associated with tables and charts.
The data is either embedded or imported from Excel, you can find the spreasheet used in this repo.

Devices sizes are defined in `App.SizeBreakpoints`, it's therefore possible to adjust the transfomration threshold to your needs.

Get the demo app from this repo: https://github.com/Feincraft/TrulyResponsive/raw/main/TrulyResponsive.msapp
How to import PowerApp from .msapp file: https://carldesouza.com/how-to-export-and-import-canvas-apps-msapp-and-zip-formats/

## Build your own apps with The Watcher
**The Watcher** is a resusable PowerApps component that lets Makers define which screens should be shown at which device size.

![](https://user-images.githubusercontent.com/32096531/166683189-94bdb755-a120-4fc6-8065-4114b1fb7e0f.png)

Makers would still need to accomodate different device sizes in the same category by stretching UX elements. For example: 5" phones and 6" phones are different in size and can have different resolutions, but not so much so that an entirely new UX is needed. Stretching tables and panels is perfectly fine. However, if we start the same app on a 10"-11" tablet, we'll need a different UX to take advantage of the space and just make the app usable.

### How it works
The Watcher can work in two modes: Fixed Screen and Adaptive.
In **Fixed Screen** mode we expect our app to run on different screen size but without them changing the app window on the fly. These can be regular phones and tablets.
In **Adaptive** mode, The Watcher will actively monitor the app state and will change the UX when needed.
This can be used in foldables (variable geometry phones, tablets, laptops) and desktops.

Select the option right for your app by swithing the Fixed Screen property.

### Considerations

- The Watcher component needs to be present on every screen for Adaptive apps and only on the starting screen of Fixed Screen apps.

- It's recommended to make the starting screen blank, to avoid flickering on initial UX switching.

- When building apps with The Watcher, select the Tablet option:
![](https://user-images.githubusercontent.com/32096531/166683667-c5622f8b-9724-4a77-a0ac-bbd72b1eaac8.png)

Don't worry the app will run perfectly on any device.

- Disable "Scale to fit", The Watcher will be handling scaling.
![](https://user-images.githubusercontent.com/32096531/166683540-5428614a-4c63-4115-a3ba-38cf5a7024a5.png)

- The Watcher takes breakpoint values from `App.SizeBreakpoints`. You can see the value and change the in your app or enable Debug Mode in The Watcher to see current values.

Start building with The Watcher component: https://github.com/Feincraft/TrulyResponsive/raw/main/TheWatcher.msapp

How to import components? You click "Import Components" 😉

![ImportComponent](https://user-images.githubusercontent.com/32096531/166683736-6badc31b-1b06-4e50-ad00-0d8d0af1fd4d.png)


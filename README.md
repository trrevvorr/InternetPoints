# InternetPoints
Displays Instagram likes and followers on a MAX7219 display using Particle Photon

### How To Set Up
This is primarily a personal project, so it'll take a little work to get it working for yourself but here's how:
1. Order a Particle Photon: [link](https://store.particle.io/products/photon)
1. Order a 5V MAX7219 LED display; [here's](https://www.amazon.com/gp/product/B06W9F1J2Z/ref=oh_aui_search_asin_title?ie=UTF8&psc=1) the one I ordered.
1. Order a momentary push button switch; [here's](https://www.amazon.com/gp/product/B00U5UBV8A/ref=oh_aui_search_asin_title?ie=UTF8&psc=1) the ones I ordered.
1. Sign up for an Instagram developer account [here](https://www.instagram.com/developer/)
	- all you need is sandbox permissions
	- note your client ID, you'll need it later
1. Flash [InternetPoints.ino](https://raw.githubusercontent.com/trrevvorr/InternetPoints/master/particle/InternetPoints.ino) to your Photon
1. Hook up the display to your Photon (Photon should be powered down)

    | MAX7219 pin | Photon pin |
    | --- | --- |
    | VCC | VIN |
    | GND | GND | 
    | DN  | D3  |
    | CS  | D2  |
    | CLK | D1  | 

1. Hook up the momentary button to your Photon (Photon should still be powered down)
	- See pin constant near top of `InternetPoints.ino` for which pin to use
1. Power up your Photon and navigate to `https://trrevvorr.github.io/InternetPoints/link/linkAccount?particle_access_token=<ACCESS_TOKEN>&particle_device_id=<DEVICE_ID>&instagram_client_id=<CLIENT_ID>` with your Particle access token, device ID, and Instagram client ID (from your developer account) inserted in to the appropriate locations.
	- I recommend creating a QR code of this link and attaching it to your device
1. Follow instructions provided by link for connecting your Instagram account to the device
1. Once linked, your display should display the sum of the likes of your last 20 Instagram posts like this:
![example device image](https://github.com/trrevvorr/InternetPoints/blob/master/00100lPORTRAIT_00100_BURST20181215002317576_COVER.jpg?raw=true)

### How To Use
1. Navigate to link (see above) to connect device to the internet and to link to your Instagram account. 
1. Press button to toggle between likes and follows

### Know Bugs
- Doesn't render properly on iOS (and probably OS X)

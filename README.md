## overview

captures distance from a sculpture using time-of-flight LIDAR (sensor = tfluna). plays different audio samples conditional upon the distance.

## gear

- raspberry pi 4 model 
- ![TF luna sensor](https://en.benewake.com/TFLuna/index.html)

## setup

`ssh cat@catolith01.local`

## dev log
### 040226
- appears to be sensitivty when connected with a USB-C adapter, and this can cause issues with serial connectivity 
- j got networking working so we can dev via `ssh cat@catolith.local`
- after trying to get `playsound` working and subsequently a ton of dependencies, switched to using `aplay` via `subprocess`
- increased "refresh rate" and removed terminal output to allow for better meowing speed, but probably need to figure out what is actually happening from a b/w perspective because it's hanging a lot


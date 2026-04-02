## overview

detects occluded distance from a sculpture using time-of-flight LIDAR. 

plays different audio samples conditional upon distance.

## gear

- Raspberry PI 4 model B
- [TF luna sensor](https://en.benewake.com/TFLuna/index.html)

## setup
### hardware
- connect tfluna sensor to raspberry pi  
- ensure the pi is connected to internet
### run from terminal
```
ssh cat@catolith01.local
python3 detect_distance.py
```

## dev log
### 04/02/26
- serial connectivity issues -- appears to drop after awhile when connected via USB-C adapter
- k no more conn issues now that it's wireless -- j got networking working so we can dev via `ssh cat@catolith.local`
- after trying to get `playsound` working and subsequently a ton of dependencies, switched to using `aplay` via `subprocess`
- increased sampling rate and removed terminal output to allow for better sensor reactivity

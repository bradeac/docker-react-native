## This repo was forked from [edy/docker-react-native](https://github.com/edy/docker-react-native)

I'm thinking of slightly modifying this Dockerfile:
- parameterised versions
- integrate an emulator into the container

# Getting started

```
git clone https://github.com/bradeac/docker-react-native
cd docker-react-native
```

## Build

```
docker build -t react-native .
```

## Run using a real device

Plug in your phone, make sure it's not in 'Charge only' mode and make sure that USB debugging (ADB) is enabled.

Navigate to the folder where you have the app code and run:
```
docker run --rm -it --name react-native -v $PWD:/app --privileged -v /dev/bus/usb:/dev/bus/usb -p 8081:8081 deredy/react-native
```

After container started:
```
react-native run-android
```

# Can Setup

Connect Kvaser USB to PC. Type:

```
sudo ifconfig -a
```

and check we have `can0` and `can1`.

Setup can channels by:

```
sudo ip link set can0 type can bitrate 500000
sudo ip link set up can0
sudo ip link set can1 type can bitrate 500000
sudo ip link set up can1
```

# Joystick Demo

## Build

Follow: https://github.com/PolySync/oscc-joystick-commander

Specifically, I am using `devel` branch at 2018-07-11 @ Suzhou.

Also, please use the following command:

```
cmake .. -DKIA_NIRO=ON
```

because we are `KIA NIRO`.

## Run

Connect Joystick USB to PC, and start joystick:

```
./oscc-joystick-commander 0
```

and we should get some `successfully` messages.
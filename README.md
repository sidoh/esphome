# esphome configurations

Collection of my [esphome](https://esphome.io/) configurations.

## Components

There are several components. Generally speaking yaml files without a `.` prefix correspond to a device.

1. `xxx_blinds.yaml`: Configurations for window blinds. Full setup described [here](https://blog.christophermullins.com/2020/02/16/automating-blinds-with-a-retrofitted-external-motor/).
2. `bed_occupancy.yaml`: A pressure based occupancy sensor.
3. `ir_blaster_*.yaml`: MQTT-driven IR blasters.


## Setup

#### Install python

Tested with the python version specified in `.python-version`, but generally should work with newer versions.

#### Install python requirements

(Optional) Create a new virtual environment first

```bash
python -m pip install -r requirements.txt
```

This should install `esphome`.

#### Setup secrets

Copy `secrets.example.yaml` to `secrets.yaml` and fill in the values.

#### Compile and upload

Compile a component using `esphome`:

```bash
python -m esphome compile office_blinds.yaml
```

Upload the compiled firmware to the device:

```bash
python -m esphome upload office_blinds.yaml
```

## Troubleshooting

If you encounter any issues during setup or operation, check the ESPHome documentation or open an issue in this repository.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

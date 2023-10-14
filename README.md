# nrf-lumen

nRF52840 NeoPixel controller board

![Render of the controller board](./nrf-lumen.png)

![Photo of the board with LED strip attached](./IMG_3479.jpeg)

## Initialization

Make sure you have a proper Zephyr development environment according to the official documentation.

```sh
west init -m https://git.leon.fyi/lumen-sdk --mr main lumen-workspace # or
west init -m https://github.com/leonrinkel/lumen-sdk --mr main lumen-workspace
cd lumen-workspace
west update
```

## Building

```sh
west build -b lumen lumen-sdk/app
```

## Flashing

```sh
west flash --runner jlink # or
west flash --runner pyocd
```

## License

Please see [hardware/LICENSE](hardware/LICENSE) and [lumen-sdk](https://git.leon.fyi/lumen-sdk). The software side of this project is based on [Zephyr](https://www.zephyrproject.org) which is mostly licensed under the [Apache-2.0](http://www.apache.org/licenses/LICENSE-2.0) license.

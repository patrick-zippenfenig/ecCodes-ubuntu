# ecCodes Ubuntu Packages

Prebuilt [ECMWF ecCodes](https://github.com/ecmwf/eccodes) packages for Ubuntu `22.04 (jammy)` and `23.04 (lunar)` available via APT repository. Supports `amd64` and `arm64`.

The prebuilt ecCodes packages are used to get the latest ECMWF ecCodes library for the open source weather api https://open-meteo.com.

```bash
curl -L https://patrick-zippenfenig.github.io/ecCodes-ubuntu/public.key | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/ecCodes-ubuntu.gpg > /dev/null
echo "deb https://patrick-zippenfenig.github.io/ecCodes-ubuntu/ jammy main" | sudo tee /etc/apt/sources.list.d/ecCodes-ubuntu.list

sudo apt update
sudo apt install libeccodes0
```

Note: Make sure to select `jammy` or `lunar` above.

Only one `libeccodes0` package is available that contains development header, GRIB tables and binaries like `grib_ls`. On the official Ubuntu ecCodes distribution they split between `libeccodes0`, `libeccodes-dev`, `libeccodes-data`, `libeccodes-tools` and `libeccodes-doc`. 


## Contributing

The ecCodes packages are build using GitHub actions and the workflow is available [here](.github/workflows/build.yml). It is using Docker with to build on `amd64` and `arm64`. The built is rather slow for `arm64`, but it works. Packages are built using [FPM](https://github.com/jordansissel/fpm) and deployed as an APT repository directly on GitHub pages.

The built a new version, a new tag (like `2.30.0`) must be pushed to this repository to trigger the workflow.

New architectures and distributions can be added on request. Please open an issue ticket.

Contributions welcome!


## License

MIT
# bmi-diffusionf

A BMI for the [diffusionf model](https://github.com/mdpiper/diffusionf).

## Build, install, and run

To build this BMI,
it's assumed that the `diffusionf` model has been built and installed.

Change to the root directory of this repository and execute:

```bash
mkdir _build && cd _build
cmake .. -DCMAKE_INSTALL_PREFIX:PATH=/path/to/diffusionf/install
make
make install
```

where **/path/to/diffusionf/install** is the location
of the installed `diffusionf` model.

After installing,
run the model through its BMI with the `run_bmidiffusionf` program,
which takes a model configuration file
(see the [examples](./examples) directory for a sample)
as a required parameter.

    run_bmidiffusionf test.cfg

Output from the model run is written to the file **bmidiffusionf.out**
in the current directory.

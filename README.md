# PlutoWebcam

Webcam Support for Pluto Notebooks based on mitmath/18S191

# Install & use

Add this package like so:

```julia
julia> import Pkg; Pkg.add(Pkg.PackageSpec(url="https://github.com/arturh85/PlutoWebcam.jl"))
```

In your Pluto Notebook first use PlutoWebcam:


```julia
using PlutoWebcam
```


Then you can bind your webcam like to a variable like this:


```julia
@bind image_bytes camera_input()
```

And convert the raw bytes to useful [RGB](https://github.com/JuliaGraphics/ColorTypes.jl):

```julia
my_face = process_raw_camera_data(image_bytes)
```

# Plans

First version is just a copy of the MITMath code but I plan to extend it with:

- Arrays of Images with a single Webcam Bind
- More Controls

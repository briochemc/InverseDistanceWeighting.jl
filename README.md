# InverseDistanceWeighting.jl

[![Build Status](https://travis-ci.org/juliohm/InverseDistanceWeighting.jl.svg?branch=master)](https://travis-ci.org/juliohm/InverseDistanceWeighting.jl)
[![CodeCov](https://codecov.io/gh/juliohm/InverseDistanceWeighting.jl/branch/master/graph/badge.svg)](https://codecov.io/gh/juliohm/InverseDistanceWeighting.jl)

This package provides a high-performance implementation of the inverse distance weighting scheme introduced in the very early days of geostatistics [[Isaaks 1990](https://www.amazon.com/Introduction-Applied-Geostatistics-Edward-Isaaks/dp/0195050134)]. It is perhaps the simplest first attempt in the literature to perform estimation based on the notion of proximity to data locations.

This implementation makes use of k-d trees from the [NearestNeighbors.jl](https://github.com/KristofferC/NearestNeighbors.jl)
package, which leads to an ultra fast estimation method for large or high-resolution spatial domains. Although this
method is recommended for fast assessment of a new field, it has poor statistical properties (no covariance model) and should mainly be used for qualitative purposes.

## Installation

Get the latest stable release with Julia's package manager:

```julia
Pkg.add("InverseDistanceWeighting")
```

## Usage

This package is part of the [GeoStats.jl](https://github.com/juliohm/GeoStats.jl) framework.

For a simple example of usage, please check [this notebook](examples/usage.ipynb).

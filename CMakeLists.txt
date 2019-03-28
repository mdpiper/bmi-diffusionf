cmake_minimum_required(VERSION 2.8)

project(bmi-diffusion Fortran)

set(bmidiffusion_lib bmidiffusionf)

# Locate the installed diffusionf library (via CMAKE_PREFIX_PATH).
find_library(diffusion_lib diffusionf)

# Locate the installed diffusion module (via CMAKE_PREFIX_PATH).
find_path(diffusion_mod diffusion.mod)
include_directories(${diffusion_mod})

add_subdirectory(bmi-diffusion)

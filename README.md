# Climate Dataset Merging Exercise

This module checken includes a hands-on practice notebook and an answer key that walk through
merging two climate datasets over a spatial domain with mismatched spatial and temporal
resolution using `xarray`.

## Learning Goals
- Stream remote NOAA reanalysis and precipitation products directly from THREDDS servers.
- Resample time coordinates and interpolate spatial grids with `xr.resample` and `xr.interp`.
- Combine harmonized variables with `xr.merge`, then explore the result via maps and
  simple diagnostics.

## Repository Contents
- `notebooks/merge_climate_datasets_exercise.ipynb` – Student version with TODO cells and
  guidance for each processing step.

## Environment
The Python environment you created in Module 2 (`xarray-climate`) already contains the
required libraries for this assignment. Activate it with:

```bash
conda activate xarray-climate
```

or the equivalent command for your environment manager, then launch Jupyter Lab or
Notebook to explore the materials.

## Getting Started
1. Open the exercise notebook and work through each section, replacing the
   `NotImplementedError` placeholders.
2. The results in the last cells that generate a visualization and a dataset are the deliverables for the Check In.

Happy merging!

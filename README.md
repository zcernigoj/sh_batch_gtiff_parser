# sh_batch_gtiff_parser

## `gtiff_parser.py` 
Contains code for parsing the geotiff that Sentinel Hub batch process API creates to your prefered format

Supports:
- geotiff
- netcdf
- zarr

Main function: `parse_multitemporal_gtiff_to_format`

Input parameters:
- `input_tiff`: url to openEO results geotiff image (`default.tif`)
- `input_metadata`: url to openEO results datacube metadata (`userdata.json`)
- `output_dir`: folder where the output files will be put
- `output_format`:  output format

```python
output_file_paths = parse_multitemporal_gtiff_to_format(input_tiff, input_metadata, output_dir, output_format)
```


## `open_file.py`
Contains functions to open files in formats
- tiff: `open_tiff("path/to/file")`
- netcdf: `open_netcdf("path/to/file")`
- zarr: `open_zarr("path/to/file")`

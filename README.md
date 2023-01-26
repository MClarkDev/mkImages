# mkImages

Batch image processing for GIMP, used to crop and scale images for different aspect ratios.

## How to use

- Create input files in gimpi.
- Run batch processor on command line
- Package images and go.
- Profit.

### Input Files

Import your image to GIMP and save as native [file].xcf format.

For each desired aspect ratio output: create a new layer (transparent) and edit the name to match the aspect ratio (16-9).

*Note*: Ensure that the actual ratio of the layer matches the ratio name or distortion may occur in the output image.

### Batch Processing

To begin the batch processing, run the script with the required arguments pointing it at a directory containing the input files.

```
$ mkImages [ratio] [resolution] [dir]

$ mkImage 16-9 1080 /path/to/dir/
```

### Output Files

Image packs will be gnerated relative to the input directory,

>$dir/render/$ratio @ $resolution/$fname.png


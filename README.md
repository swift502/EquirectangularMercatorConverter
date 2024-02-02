![](data/preview.png)

# Equirectangular-Mercator Projection Converter

Bi-directional image projection converter. Single-script, readable Python.

Converts images between equirectangular and mercator projections. Expands the image to new aspect ratio and fills in missing pixels using nearest sampling.

### Usage

1. Install [Python 3.11+](https://www.python.org/downloads/)
1. Install requirements
    ```
    pip install -r requirements.txt
    ```
1. Run the [demo script](demo.py)
    ```
    python demo.py
    ```

### Limitations

The conversion process can't handle latitude angles of 85+ degress well. Images converted to mercator will have 5 degree sections around poles cropped, while images converted to equirectangular have a stretched 5 degree strip on top and bottom.

### Performance

Conversion can take a long time for larger images. PyPy might be a lot faster, I haven't tested it though.

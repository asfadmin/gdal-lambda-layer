# About

   This project builds and deploys an AWS Lambda layer that supports GDAL 3.0.4 for Python 3.8.1.

# Build the Layer

   `aws cloudformation deploy --stack-name gdal-layer --template-file cloudformation.yaml --capabilities CAPABILITY_NAMED_IAM`

   `aws codebuild start-build --project-name gdal-layer`

# Use the Layer

   1. Create a new lambda function with the python 3.8 runtime
   1. Attach the layer to your function
   1. Set environment variable `GDAL_DATA=/opt/lib/data`
   1. Add `from osgeo import gdal` to your function code
   1. Enjoy!

# Additional Resources

   [Geospatial Data Abstraction Library](https://www.gdal.org/)

   [GDAL on PyPI](https://pypi.org/project/GDAL/)

   [AWS Lambda Layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)

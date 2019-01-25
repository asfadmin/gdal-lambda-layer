# About

   This project builds and deploys an AWS Lambda layer that supports GDAL 2.4.0 for Python 2.7.

# Build the Layer

   `aws cloudformation deploy --stack-name gdal-layer --template-file cloudformation.yaml --capabilities CAPABILITY_NAMED_IAM`

   `aws codebuild start-build --project-name gdal-layer`

# Use the Layer

   1. Create a new lambda function with the python 2.7 runtime
   1. Attach the layer to your function
   1. Set environment variable `GDAL_DATA=/opt/lib/data`
   1. Add `from osgeo import lambda` to your function code
   1. Enjoy!

# Additional Resources

   [Geospatial Data Abstraction Library](https://www.gdal.org/)

   [GDAL on PyPI](https://pypi.org/project/GDAL/)

   [AWS Lambda Layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)

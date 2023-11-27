# api-gateway-talk-dependencies
AWS lambda dependencies for API Gateway talk in Pydelhi Meetup

## Pre-requisite
1. Configure AWS profile
2. Install AWSume
3. Install nodeJS 20.X
4. Install Python 3.10.x

## How to run the setup
1. Install NPM package
```bash
npm install
```
2. Navigate to dependencies folder
```bash
cd api_gateway_dependencies
```
3. Create python layer
```bash
pip install -r requirements.txt -t python/lib/python3.10/site-packages --platform manylinux2014_x86_64 --only-binary=:all: --implementation cp
```
4. Deploy the package from the root folder
```bash
cd ..
serverless deploy
```
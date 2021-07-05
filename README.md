# esp_tfmicro
## Get tfmicro component for esp
This Dockerfile generate tfmicro component for futher usage in esp project. 
Guide:
1) Build docker container. 
```
docker build . -t tflite-generator
```
You can specify version of esp-idf or tensorflow with --build-arg parameter (i.e. --build-arg tensorflow_version=2.4.0 --build-arg esp_idf_version=release/v4.3)
2)Run docker container.
```
docker run -v $PWD/component:/dst -t tflite-generator
```
3)Move component folder into your esp_project folder
```
sudo mv ./component/ PROJECT_PATH/
```

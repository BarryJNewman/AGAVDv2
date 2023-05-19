# AGAVDv2
docker build -f Dockerfile -t myavdbuilder .

docker save -o ./myimage_latest.tar myavdbuilder

#Loaded image: myavdbuilder:latest
docker load -i ./myimage_latest.tar

docker run --rm -it --entrypoint bash myavdbuilder


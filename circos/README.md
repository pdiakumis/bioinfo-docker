# Dockerized  [CIRCOS](http://www.circos.ca/)

Taken from <https://github.com/alexcoppe/bio-dockers/blob/master/circos/README.md>


## Usage

### Docker Pull Command

```
docker pull pdiakumis/circos
```

### Example

To run an example from the circos package, download the original CIRCOS package and decompress it:

```
wget http://circos.ca/distribution/circos-0.69-3.tgz
tar xzvf circos-0.69-3.tgz
```

Copy the `data` and the `etc` directories from the CIRCOS distribution to the current directory: 

```
cp -R  circos-0.69-3/example/data .
cp -R  circos-0.69-3/example/etc .
```

Copy the CIRCOS configuration file to your current directory:

```
cp  circos-0.69-3/example/etc/circos.conf .
```

Run the docker container:

```
docker run --rm -it -v $(pwd):/data pdiakumis/circos -conf /data/circos.conf -outputdir /data
```

The command takes approximately 30 seconds to finish. 
You will find the `circos.png` figure in the current directory


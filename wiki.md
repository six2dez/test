# ReconFTW

## Table of Contents
* [Installation Guide](#Installation-Guide)
* [Post Installation Guide](#Post-Installation)
  * [Amass Config](#Amass-Config)
  * [Subfinder Config](#Subfinder-Config)
  * [Git-hound Config](#GitHound-Config)
  * [Favup Config](#Favup-Config)
  * [SSRF Server](#SSRF-Server)
  * [Blind XSS Server](#Blind-XSS-Server)
  * [Github Token](#Github-Token)
  * [Subfinder Config](#snapcraft)
 

# Installation Guide
# 
#
## Configuring Go
#  
### From Binary
```sh
$ wget https://golang.org/dl/go1.15.7.linux-amd64.tar.gz
$ tar -C /usr/local -xzf go1.15.7.linux-amd64.tar.gz
```
### Configuring $PATH
Add the following lines in your .bashrc/.zshrc/../.../../../
```bash
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
```
 ### Clone reconFTW from git 
```sh
$ git clone https://github.com/six2dez/reconftw.git
$ cd reconFTW
$ chmod +x *.sh
$ ./install.sh
```

# Post Installation Configuration
#  
## Amass Config
You will need a config file to use your API keys with Amass
See the [Example Configuration File](https://github.com/OWASP/Amass/blob/master/examples/config.ini) for more details.
| Operating System | Path |
| ---------------- | ---- |
| Linux / Unix |  `$HOME/.config/amass/config.ini` |

## Subfinder Config
Subfinder to work with certain services, you will need to have setup API keys
| Operating System | Path |
| ---------------- | ---- |
| Linux / Unix |  `$HOME/.config/subfinder/config.yaml` |

## Git-hound Config
Create a  `~/.githound/config.yml` with your GitHub username and password. Optionally, include your 2FA TOTP seed. See [config.example.yml](config.example.yml).

## Favup Config
Run the following command 
`shodan init [Your-API-Key]`


















### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MORE Tests
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>

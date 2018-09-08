# CA-Toolbox
CA-Toolbox permit to create and manage easily a certificate authority without having knowledges on _cfssl_ and _openssl_ commands.

On our templates, every certificate are in ```RSA 4096bits```, the _root_ and the _intermediate_ certificate have a life time of _15 years (131400h)_ and every _client_ certificate have a life time of _1 year (8760h)_.

_Note:_ At this moment, our templates don't have _OCSP_ configuration. If you need this functionnality, don't hesitate to poke me or make a _pull request_.

_Note 2:_ I plan to make three new tools to generate the configuration file instead of manually editing each file.

# Prerequisites
For using CA-Toolbox, you need to have:
 * Linux machine
 * Bash
 * openssl
 * Go ([https://golang.org/doc/install](https://golang.org/doc/install))
 * cfssl ([https://github.com/cloudflare/cfssl#installation](https://github.com/cloudflare/cfssl#installation))

# Usage
 > **Warning:** this first commit are a first push. The documentation are not finished (but it's easy to use without the documentation)
 > Steps:
 >  1-1 copy root_ca.json.tpml and rename to root_ca.json and edit them for using you values
 >  1-2 gen-root
 >  2-1 copy intermediate_ca.json.tpml and rename to intermediate_ca.json and edit them for using you values 
 >  2-2 gen-intermediate
 >  2-1 copy client_cert.json.tpml and rename to client_cert.json and edit them for using you values  
 >  3-2 gen-client
 >  4 gen-crt 
 >  5 retrieve crt files in exports folder and install them in the system 

Clone the repository anywhere you want on your machine (we will use ```/opt/ca-toolbox``` for the example):
```
git clone https://github.com/themimitoof/ca-toolbox /opt/ca-toolbox
```

You need to configure the environment variable ```CAFOLDER``` to make ca-toolbox functionnal:
```
export CAFOLDER=/opt/ca-toolbox
```

Now, browse into ```$CAFOLDER/conf``` folder, create a copy of ```root_ca.jon.tmpl```, rename it in ```root_ca.json``` and edit it.

# Install CA on the system
For installing the root and the intermediate certificate on your system or on the browser, you need to generate a _comprensible_ certificate for the system. For this, you need to need use the command ```gen-crt``` and follow the instruction for your system.

## Windows
ds

## Linux
ds

## Mac OS
ds

# License
This toolbox are release with MIT license.
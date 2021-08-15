# cloud9.env

Set up, config, tips for cloud ide usage


## Environment additions

sudo yum install sudo

## Github config 

See [here](https://medium.com/sonabstudios/setting-up-github-on-aws-cloud9-with-ssh-2545c4f989ea)

Note: use ssh for cloning, not https.

Also note you will need to configure you git user name and email, e.g.

```
    git config --global user.name "Your Name"
    git config --global user.email you@example.com
```

## Kafka Setup

Note - assumes a single cluster... or that you want the first one in the list...

```
# In the env file
. ./kafka.env
```

## Java and Mvn

Install mvn

```
sudo wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo
sudo sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo
sudo yum install -y apache-maven
```

Now repair java via `sudo alternatives --config java` to select Java 11 instead of the manky Java 7 that gets installed with mvn for who knows what reason.

## Misc Tips

Shut it down - sudo poweroff

## Serverless framework

npm install -g serverless

## Node

Update node js

Node instructions available [here](https://docs.aws.amazon.com/cloud9/latest/user-guide/sample-nodejs.html)
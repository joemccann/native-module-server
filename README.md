# SYNOPSIS

Native module directory server for AWS Lambda supported native node modules.

## USAGE

If you haven't already, create an [EC2 instance using AWS Linux AMI version 2](https://medium.com/@nishankjaintdk/setting-up-a-node-js-app-on-a-linux-ami-on-an-aws-ec2-instance-with-nginx-59cbc1bcc68c).

Then, ssh into the server:

```sh
ssh scp -i ~/path/to/your/keys.pem ec2-user@YOUR-EC2-IP-ADDRESS
```

Next, install the native node module in the `/tmp` directory.

```sh
sudo su -
cd /tmp
npm i node-canvas
zip -r node-canvas.zip node_modules
```

Now, download the entire directory via SCP:

```sh
scp -i ~/path/to/your/keys.pem ec2-user@YOUR-EC2-IP-ADDRESS:/tmp/node-canvas.zip .
```

## LICENSE

MIT

# Trusted known_hosts

Be certain about the authenticity of your used services.

## How-to-Use

Clone this repository. In this tutorial, it is assumed that you have cloned this repo into `$HOME/.ssh/`
```
git clone https://github.com/tsbauer/trusted_known_hosts.git
```

Then add the following line to your ssh `config` and substiture your desired `SERVICE`
```
UserKnownHostsFile $HOME/.ssh/known_hosts $HOME/.ssh/trusted_known_hosts/SERVICE
```

Once configured, if you ever encounter a prompt for checking the host key when using trusted services you should be very suspicious.

It is a better practice to fail the ssh operation if the service is unknown.
```
StrictHostKeyChecking yes
```

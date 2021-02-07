## signal-tls-proxy

BastilleBSD template to bootstrap signal-tls-proxy

## Bootstrap

```shell 
bastille bootstrap https://gitlab.com/ddowse/signal-tls-proxy 
```

## Usage

Bastille's redirection command and the related argument "SSLPORT" can set as needed.

```shell
# Redirects tcp port 80 on host to 80 on jail this is mendatory for issuing the certificate 
bastille rdr TARGET 80 80 
# Redirects tcp port 443 on host to 443 on jail
bastille rdr TARGEt 443 443 
bastille template TARGET ddowse/signal-tls-proxy --arg EMAIL=user@example.com --arg DOMAIN=FQDN --arg SSLPORT=443
```

## Extra

Adds also a Cronjob to reissue certificate 

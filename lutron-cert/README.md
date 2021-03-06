# Home Assistant Community Add-on: Lutron Certificate

[![Release][release-shield]][release] ![Project Stage][project-stage-shield] ![Project Maintenance][maintenance-shield]

[![Discord][discord-shield]][discord] [![Community Forum][forum-shield]][forum]

[![Buy me a coffee][buymeacoffee-shield]][buymeacoffee]

A simple utility to generate signed certificate files to allow local control of
a Lutron Caseta smart bridge.

## About

This add-on will guide you through the necessary steps to create signed
certificate files necessary to control your Lutron Caseta smart bridge with
Home Assistant.

Three files will be created during successful execution of the wizard:

- `/ssl/lutron/caseta.key`: the private key file used to generate the
  certificate.
- `/ssl/lutron/caseta.crt`: the signed certificate file used to connect to
  the Lutron Caseta bridge.
- `/ssl/lutron/caseta-bridge.crt`: the certificate authority file that is
  downloaded from the Lutron Caseta bridge.

Be sure to add Lutron Caseta to your `configuration.yaml` after starting the
add-on:

```yaml
lutron_caseta:
  host: 192.168.1.100
  keyfile: /ssl/lutron/caseta.key
  certfile: /ssl/lutron/caseta.crt
  ca_certs: /ssl/lutron/caseta-bridge.crt
```

For more information on how to configure Lutron Caseta in Home Assistant see
the [Lutron Caseta documentation][lutron-caseta-docs].

## WARNING! THIS IS A BETA VERSION!

This Home Assistant Add-ons repository contains beta releases of add-ons.

- They might stop working at any time.
- They could have a negative impact on your system.

This repository was created for:

- Anybody willing to test.
- Anybody interested in trying out upcoming add-ons or add-on features.

If you are more interested in stable releases of our add-ons:

<https://github.com/hassio-addons/repository>


[buymeacoffee-shield]: https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-2.svg
[buymeacoffee]: https://www.buymeacoffee.com/dale3h
[discord-shield]: https://img.shields.io/discord/478094546522079232.svg
[discord]: https://discord.me/hassioaddons
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg
[forum]: https://community.home-assistant.io/t/home-assistant-community-add-on-lutron-certificate/70317?u=frenck
[lutron-caseta-docs]: https://www.home-assistant.io/components/lutron_caseta/
[maintenance-shield]: https://img.shields.io/maintenance/yes/2020.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[release-shield]: https://img.shields.io/badge/version-v0.5.2-blue.svg
[release]: https://github.com/hassio-addons/addon-lutron-cert/tree/v0.5.2
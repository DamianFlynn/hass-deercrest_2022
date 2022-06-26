# Home Assistant Configuration Files 

<p align="center">
  <img src="./.assets/logo.png">
</p>

<p align="center">
    <a href="https://github.com/damianflynn/home-assistant/actions" alt="Pipeline">
        <img src="https://github.com/damianflynn/homeassistant/workflows/Home%20Assistant%20CI/badge.svg" /></a>
        <a href="assets/current_ha_version.svg" alt="Currently Running">
        <img src="assets/current_ha_version.svg" /></a>
        <a href="https://www.home-assistant.io/latest-release-notes/" alt="Latest HA Version">
        <img src="https://img.shields.io/badge/dynamic/json?label=Latest%20HA%20Version&query=%24.info.version&url=https%3A%2F%2Fpypi.python.org%2Fpypi%2Fhomeassistant%2Fjson" /></a>
        <a href="https://github.com/damianflynn/homeassistant" alt="Last Commit">
        <img src="https://img.shields.io/github/last-commit/damianflynn/homeassistant" /></a>
        <a href="https://github.com/damianflynn/homeassistant/stargazers"><img src="https://img.shields.io/github/stars/damianflynn/homeassistant.svg?style=plasticr"/></a>     
</p>

<p align="center">
   <a href="https://buymeacoff.ee/damianflynn" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
</p>

# Introduction
I discovered [Home Assistant](https://www.home-assistant.io) in 2017 and have been slowly adding to it since then.

## The Home Assistant Server
I run a dedicated Intel NUC, with HAAS OS Intel(R) Core(TM) i7-2600 CPU @ 3.40GHz 8GB


# Automations

*

# Hardware Running in my Home Assistant Setup:

# Continuous Integration Continuous Deployment
I use GITOPS principals, and when I commit a change to this repo it kicks off an [automatic test](https://github.com/damianflynn/homeassistant/actions) of the config using a Home Assistant environment, which will when completed sucessfully

See [the config here](https://github.com/damianflynn/homeassistant/blob/master/.github/workflows/push-notifiy-hass.yml).

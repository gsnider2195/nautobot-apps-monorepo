# Apps Monorepo

<p align="center">
  <img src="https://raw.githubusercontent.com/gsnider2195/nautobot-apps-monorepo/develop/docs/images/icon-apps-monorepo.png" class="logo" height="200px">
</p>

## Overview

This is a docker compose project to allow development of multiple Nautobot apps in a single repository. It is based on the standard Nautobot App invoke/docker workflow so you should be able to clone this repo, run `invoke build migrate debug` and have a working Nautobot instance with all of the discovered Nautobot apps on your local system installed.

### Directory Structure

By default, this project will iterate through all of the sibling directories within its parent directory for Nautobot apps to install. For example if you have the following directory structure:

```
/github/nautobot/nautobot-apps-monorepo  # This repository
/github/nautobot/nautobot-app-1
/github/nautobot/nautobot-app-2
```

Then both `nautobot-app-1` and `nautobot-app-2` will be installed into the Nautobot instance.

This can be customized using the `invoke.yml` file and customizing the `app_directories` variable. See the `invoke.example.yml` file for an example.

## Questions

For any questions or comments, please check the [FAQ](https://docs.nautobot.com/projects/apps-monorepo/en/latest/user/faq/) first. Feel free to also swing by the [Network to Code Slack](https://networktocode.slack.com/) (channel `#nautobot`), sign up [here](http://slack.networktocode.com/) if you don't have an account.

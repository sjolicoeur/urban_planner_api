# Overview

Urban Planner is a jail orchestration system, meant to provision jails on a single node and later on multiple nodes. Provisionned jails will be wired up for the user to be fronted by a local load-balancer, basic logging, ssh capabilities, ssh port forwarding and extendable sidecars for maintenance (see DRiD).

# Installation

Deploy one of the made images:
- DigitalOcean
- AWS
- GCP

Or manually by using the DRiD script in the `deploy` folder.

# Deploying the demo app

To deploy an application make use of the Urban Planner CLI.
- cd into your project
- `up blueprint init` to create an empty urban planner config file that will be use for your application
- edit the `.blueprint.yml` specifying your type of project `nodejs`, `python`, `php` or `java`. (note: because the jail runs on FreeBSD there may be issues with some compiled dependencies not being available)
- when ready to deploy issue `up condo deploy` you should be presented with  logs of what is happening.
- to see a list of running condos `up condo list`
- `up condo logs <condo name>` to view the current logs from the `<condo name>`



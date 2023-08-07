# notes

## Overview
This repository is designed to help deploy a stack of monitoring tools, more specifically:

- [Prometheus](https://prometheus.io/)
- [Grafana](https://grafana.com/)
- and [AlertManager](https://prometheus.io/docs/alerting/latest/alertmanager/)

For the test deployment it uses:

- [Vagrant](https://www.vagrantup.com/)
- [Virtualbox](https://www.virtualbox.org/)
- and [Ansible](https://docs.ansible.com/)

For easier deployment I use
- [GoTasks](https://taskfile.dev/)
- and [Brew](https://docs.brew.sh/Installation) package manager _(if you are not fond of this tool, you can install the packages listed in `Taskfile.yml`-s init section!)_

## Getting started

I recommend the following steps:

- install `Virtualbox`
- install Tasks - <https://taskfile.dev/installation/>
- run `task -l` to see the available tasks
- start with `task init` to set up the workstation

<details>
<summary>some notes on Virtualbox</summary>

I have not included installation steps for Virtualbox. The main reason behind this is:

- if you are a using Linux or Mac, chances are you are using everything in the same terminal --> installing `Virtualbox` should be trivial with your favorite package manager
- if you are in the same situation like I am - using Windows laptops mostly - then you will have some challenges:
    - you will need to run `Virtualbox` on the Winodws OS
    - but Ansible wont work on Windows --> you need to run that from `WSL2`
    - `Vagrant` would work on both, but you probably want to run it on `WSL2`
the solution for this is mostly described here: <https://developer.hashicorp.com/vagrant/docs/other/wsl> - but might require some tweaking / troubleshooting on your end...

</details>


## References / inspirations

<https://www.padok.fr/en/blog/prometheus-monitoring-ansible>

<https://www.ansiblefordevops.com/>

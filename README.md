# CarbonCrush test bench server setup

🛠 Configure a server to act as the Carbon Crush test bench, to allow the measure of energy consumption in Gitlab-CI.

See also [Eco-design software by measuring energy usage in Continous Integration](https://demeringo.gitlab.io/blog/sustainable_it/2022/03/08/CarbonCrush-tracking-energy-usage-of-software-branches.html) for more background.

## Content

This works with a server using Ubuntu LTS (and likely a Debian).

- Ansible script to depoy gitlab-ci runner a to execute [Scaphandre](https://github.com/hubblo-org/scaphandre) in CI.
- TODO: Terraform scripts to build the hosting server.

## Usage

### On local machine

```sh
sudo apt install -y ansible
ansible-galaxy install riemers.gitlab-runner
```

Update inventory (copy and adapt host_sample.yml into hosts.yml)

Test ansible

```sh
# Simple ping command to validate connection with the target servers
ansible -i hosts.yml --private-key ../id_scaph_rsa  all -m ping
```

Update the settings of the runner(s) in /vars/main.yml

```sh
# Execute the full playbook
ansible-playbook --private-key ../id_scaph_rsa main.yml -i hosts.yml
```

## Thanks

- https://github.com/riemers/ansible-gitlab-runner/

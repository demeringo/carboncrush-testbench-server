# CarbonCrush test bench server setup

🛠 Configure a server to act as the Carbon Crush test bench, to allow the measure of energy consumption in Gitlab-CI.

See also [Eco-design software by measuring energy usage in Continous Integration](https://demeringo.gitlab.io/blog/sustainable_it/2022/03/08/CarbonCrush-tracking-energy-usage-of-software-branches.html) for more background.

## Content

- Ansible script to depoy gitlab-ci runner a to execute [Scaphandre](https://github.com/hubblo-org/scaphandre) in CI.
- TODO: Terraform scripts to build the hosting server.

## Thanks

- https://github.com/riemers/ansible-gitlab-runner/

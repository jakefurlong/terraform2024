# Module 1 Notes

Here are my notes from the intro video!

## Where does Terraform fit into the bigger picture?

What is DevOps?

Dev --> Ops: Devs write the application code and Ops writes the operational code, but they both need to work together. 

It's a set of processes, ideas, and techniques. Everyone has a different definition, but they have one thing in common: make software delivery vastly more efficient. You don't need to know much of anything about DevOps to pass the exam, just how to automate with Terraform. Just know that the goal is to automate as much of the software delivery as possible.

What is IaC?

Write and execute code to define, deploy, update, and destroy your infrastructure. Treats ops as software. This could be:

- Ad hoc scripts (Bash, Python: gives you flexibility, but that can lead to a lack of consistency
- Config mgmt tools (Ansible, Chef, Puppet): strong consistency and API structure, idempotence, distribution
- Server templating tools (Docker, Packer, Vagrant) - immutable infra can be thrown away
- Orchestration tools (Kubernetes, Swarm, Nomad, AWS ECS)
- Provisioning tools (Terraform, CloudFormation, Pulumi)

What are the benefits of IaC?

- Self-service: no need for the one person that knows everything, devs can kick off their own deployments
- Speed and safety: automated and repeatable
- Documentation: anyone can read source files
- Version Control
- Validation: review code, test, static analysis
- Reuse: modules
- Happiness: less outages, focus more on coding

How does Terraform Work?

Open source tool written in Go. Compiled into single binary called "terraform" which can be installed on your laptop or a build server. Under the hood, Terraform makes API calls on your behalf to one or more providers such as AWS, Azure, GCP, etc. You write your terraform configurations and Terraform passes that to the provider using the API to provision what you requested. Terraform maintains an account of what you last provisioned with a state file. Future changes will compare your resources to the state file to look for differences.

How does Terraform compare to other IaC tools?

Here are the trade-offs to consider:

- Config mgmt versus provisioning
- Mutable infra vs. immutable infra
- Procedural vs. declarative language
- General purpose language vs. domain-specific language
- Master vs. masterless
- Agent vs. agentless
- Paid vs. free
- Large community vs. small community
- Mature vs. cutting edge
- Use of multiple tools together

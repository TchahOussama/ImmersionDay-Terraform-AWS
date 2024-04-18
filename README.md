Lab (TFE = TFC)

Terraform Cloud Organization

Project < Workspaces

Remote execution => manage runs (executions) in TFE (like pipelines)

Manage access to TFE (Teams, Users, Membership, Access) (> invited users to your org

Variables (workspace) / Variable Sets (org level, reusable, like 
aws creds)

VCS integration for code reviews => add code to VCS tools (like github) [resource "tfe_oauth_client" "github"] 
Terraform Cloud registers webhooks with your VCS provider, then automatically queues a Terraform run whenever new commits are merged to the branch of the linked repository.
https://github.com/TchahOussama/hashicat-app/settings/hooks

Sentinel policy-as-code (example for tags obligation, billing control) [resource "tfe_policy_set" "test"]

Private Registry (to publish custom modules)
You can publish modules from TFE console or via code [resource "tfe_registry_module"]

Terraform Cloud API: API calls to our Terraform Cloud organization and workspaces (from CI/CD tool for example)
HTTP API Core / TFE Terraform Provider / CDK for Terraform
Automation with wrappers (veding_macheen) / Automation with CI/CD

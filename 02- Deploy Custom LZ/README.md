# CAF-Terraform-Examples
This page describes how to deploy your Azure landing zone with a custom configuration, including guidance on how to customize the Management Group hierarchy.

In this example, we take the default configuration and make the following changes:

Create a new custom archetype definition named customer_online which will create two Policy Assignments, Deny-Resource-Locations and Deny-RSG-Locations at the associated scope with a set of pre-configured default parameter values.
Add a new Management Group for standard workloads using the customer_online archetype definition:
Management Group ID: myorg-online-example-1
Management Group Name: MYORG Online Example 1
Parent Management Group ID: myorg-landing-zones
Allowed location list: default
Add a new Management Group for geo-restricted workloads using the customer_online archetype definition:
Management Group ID: myorg-online-example-2
Management Group Name: MYORG Online Example 2
Parent Management Group ID: myorg-landing-zones
Allowed location list: ["eastus"]
IMPORTANT: Ensure the module version is set to the latest, and don't forget to run terraform init if upgrading to a later version of the module.

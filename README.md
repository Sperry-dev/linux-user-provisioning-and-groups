# Linux User Provisioning & Group Management

## Scenario

A request was received to onboard two new employees to the Development Team. User accounts needed to be created, passwords assigned, and group membership verified.

## Objective

Create user accounts, assign users to the correct group, configure passwords, and verify access.

## Commands Used

```bash
sudo groupadd devteam
sudo useradd -m -s /bin/bash alice
sudo useradd -m -s /bin/bash bob
sudo usermod -aG devteam alice
sudo usermod -aG devteam bob
echo "alice:password" | sudo chpasswd
echo "bob:password" | sudo chpasswd
groups alice
groups bob
```
## Verification

The groups command confirmed both users were assigned to the devteam group.

```text
alice : alice devteam
bob : bob devteam
```

## Skills Demonstrated

- User Provisioning
- Group Management
- Password Administration
- Access Verification
- Linux Administration
- Technical Documentation

## Real-World Equivalent

This lab demonstrates user onboarding and access management concepts commonly performed in enterprise environments such as Active Directory and Microsoft Entra ID.

# kubernetes-coreos-do 1.0.5

### Installation
Walkthrough for setup Kubernetes on CoreOS on DigitalOcean.

### Create Master Instance

Create a new droplet via DO interface, and choose following options
1. Droplet Hostname: master
1. Select Size: Any
1. Select Region: Any with private networking support
1. Available Settings: "Private Networking", "Enable User Data"
1. Put cloud-config to user data textarea
1. Select Image: CoreOS (stable)
1. Choose you SSH key
1. Press a "Create a Droplet" button

### Create Node Instance

Create a new droplet via DO interface, and choose following options
1. Droplet Hostname: master
1. Select Size: Any
1. Select Region: Any with private networking support
1. Available Settings: "Private Networking", "Enable User Data"
1. Put cloud-config to user data textarea
1. Set `<master-private-ip>` of master node in cloud config
1. Select Image: CoreOS (stable)
1. Choose you SSH key
1. Press a "Create a Droplet" button

### Checking
* Connect to master `ssh core@%MASTER_DROPLET_EXTERNAL_IP%`
* `fleetctl list-machines` or `kubectl get nodes`

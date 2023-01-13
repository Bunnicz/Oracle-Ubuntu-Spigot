# Oracle-Ubuntu-Spigot
Short hands on tutorial how to set up your private minecraft server on Oracle Cloud Platform with your "Always Free" Tier.

[TOC]

### Create free account

Go to the official website of Oracle Cloud Platform and sign up.

Link: https://signup.cloud.oracle.com/

### Crete compute instance

Settings:

**Name:** *your compute instance name here*
**Placement:** Choose depending on availability. 

*Note: For some domains it can take a while to set up your instances.*

**Image and shape**: Canonical Ubuntu 20.04; Ampere, VM.Standard.A1.Flex, 2 OCPUs, 12 GB of memory;

*Note: All tenancies get the first 3,000 OCPU hours and 18,000 GB hours per month for free for VM instances using the VM.Standard.A1.Flex shape, which has an Arm processor. For Always Free tenancies, this is equivalent to 4 OCPUs and 24 GB of memory.*

**Networking**: If its your first compute instance choose *Create new virtual cloud network* and *Create new public subnet*. Else choose the one you have created before.
**Add SSH keys**: Paste public keys. Use *PuTTY* to generate SSH keys (If you do not have PuTTY install it from official website, it will be needed later on to configure our instance).
1. Run PuTTYgen (PuTTY Key Generator)
2. Click "Generate" and move your mouse over blank space to generate the key.
3. Provide "Key passphrase" and "Confirm". It will be used as a password for your key.
4. Click "Save private key" and choose destination.
5. Copy "Key fingerprint", go back to the Oracle Cloud Platform and paste it to the "SSH keys" field

**Boot volume**: Use in-transit encryption.

Finally click "Create" button and wait a while for a instance to be provisioned.

### Login to instance with SSH

1. Run PuTTY.
2. In the "Category" window go to Connection -> SSH -> Auth -> Credentials. Provide your private key file access path.
3. Go back to "Session" and type "Host name": ubuntu@<your-instance-IP-address>, Port: 22.
4. Save your settings by typing the name in the saved sessions field and click "Save". Now new entry should show up with your chosen name. From now on you can use those settings by loading them on your next sessions.
5. Start the connection by clicking "Open". If everything went good new window will show up with the prompt to provide your passphrase to the SSH key. Type it in and press "Enter". Now we can configure our instance.

### Instance configuration (SSH)

#### Set up without SSH key (Optional)

It is possible to login with PuTTY to your instance without SSH key. It is totally optional and you can skip this point.

#### Ubuntu update/upgrade

#### Configure instance firewall and subnet Ingress Rules on oracle cloud panel

#### Install Java OpenJDK 17 and Git

#### Create a custom user

#### Download and install Spigot

#### Start Spigot server

#### Configure Spigot as a service

#### Check minecraft server avaibility

#### Customize Server Properties

#### Install Plugins

#### Pufferpanel instalation (optional)


***###IN PROGRESS###***

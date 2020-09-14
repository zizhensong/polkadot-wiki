---
id: maintain-guides-validator-community
title: Validator Community Overview
sidebar_label: Validator Community Overview
---

## Building a Community and Attracting Nominations

After [setting up a validator][], nominations will not come in without extra work. The community of nominators will need to know about the validator in order to trust staking with them, and thus the validator must distinguish themselves in order to attract nominations. The following gives some general guidance on different approaches to take in building a community and attracting nominations.

Being a high quality validator entails not only running nodes, but also building a brand,
reputation, and community around validation services. The responsibilities of a quality validator
additionally include marketing oneself and participating in the greater community.
Becoming a known pariticipant throughout the ecosystem is a great way to attract nominations and
solidify longevity and sustainability as a validator.

One thing to keep in mind is there is a risk involved in staking for both validators and nominators,
as both can lose up to 100% of their funds if a validator gets slashed. This means it is paramount
for nominators to only nominate validators that they trust, as well as for validators to do their
best to instill confidence in their ability to provide validation services. Validators should do
their best to build a reputation through many different means, as this is one of the most important
factors in how nominators should pick who they stake with.

## Gaining Visibility

Nominators should be able to know who they are staking with. If nominators stake with a bunch of
pseudo-anonymous addresses because it seems profitable, they expose themselves to more risks than
nominating validators that follow best practices who they _know_ the addresses belong to.
Establishing a clear identity in multiple places can help gain visibility across the ecosystem. This
includes setting an on-chain identity and making a known presence throughout various community
channels.

### Setting an On Chain Identity

All validators should set an on-chain [identity][] and get a judgement on the identity so that
nominators can find nodes when browsing through various dashbaords and UIs. When someone interacts
with the chain, it ensures that an address they may come across belongs to the validator, and
actions of that identity throughout various parts of the ecosystem (staking, governance, block
explorers, etc) form a cohesive representation of their participation.

> _Note: When running multiple validator nodes, the best way to scale an identity is to use multiple
> sub-identities from a single verified identity._

### Website

One thing that can help get some visibility is setting up a dedicated site for your validator, which
includes the networks that one is a validator for and validator details such as addresses,
commission, and so forth. Including the all suggestions from this page are potential content to include in the site. After setting up a website, a validator should include this website in the corresponding field in their identity so nominators can find it easily.

## Transparency & Establishing Trust

Considering the risks involved for both Validators and Nominators, establishing trust is one of the
most important factors in building up validator services.

### Updating on Time

Both Polkadot and Kusama releases are published
[here](https://github.com/paritytech/polkadot/releases). Validators are expected to upgrade thier
nodes as soon as a new release comes out. Although not every release is mandatory to upgrade to,
each new release usually has bug fixes, optmizations, new features, or other beneficial changes.
It's within the best interest of the entire network that validators update their nodes in a timely
fashion. This signals to nominators that a validator is timely, cares about their operations, and is
quick to adapt to necesarry circumstances.

### Comission & Rewards

What does your validator charge as comission and how did you come to this number? It can be helpful
to be transparent about the long term plans around the business models of running a validator,
including the costs for infrastructure and man hours involved in maintaining operations. As many
validators will charge low comissions that often do not cover costs, outlining what comission is
charged and why can help justify higher comission rates.

Besides the current commission, it would be helpful to describe the _range_ of commission charged,
as nominators can know what to expect in the case that the rate goes up or down. Nominators may 
want to nominator a validator with a very narrow commission percent range, as this signals stability
in a validator's operations and business plans.

Another factor to consider is that claiming rewards for both the validator and nominator is not
automatic. Rewards must be claimed manually or set up in an automated way. Validators are suggested
to claim rewards on behalf of their nominators, and be transparent about how often claiming will
happen. A nominator may be more likely to stake with a validator that claims rewards daily instead
of one that doesn't claim rewards at all.

### Architecture

One aspect of building trust is being transaparent about your validator infrastructure. If
nominators know that you are running a tight ship that is focusesd on security, they are more likely
to trust you compared to those that do not disclose their infrastructure.

Some factors of architecture to highlight might include:

#### Automation approaches (terraform, ansible, chef, puppet, kubernetes, etc)

What kind of approach is taken for spinning up and provisioning nodes? How might you automate
spinning up large clusters of nodes and upgrading them? Elaborating on what kind of automation (or
lack thereof) can help get a sense of how

#### Logging, metrics, monitoring, and observability

Good node operators keep tabs on how their systems are running. Observabability is one of the most
important aspects of understanding the performance and behavior of

##### Health checks and alerting conditions

Similar to the last point,

##### Key handling policies

It is paramount that session keys and stash/controller keys are stored and handled with the utmost care, as a compromise of these can get both validator and nominator slashed. Outlining how keys are handled, how they are stored, who has access to them, and the overall policies and procudures around these is a great point of reference for nominators to gauge how comfortable they are with the security a validator takes.

##### Failover, backup, and high availability approaches

What happens when the server goes down, the process crashes, or 

##### Scenario runbooks

There are many scenarios that happen routinely, such as upgrading nodes, restoring backups, or
moving servers. Creating runbooks and sharing the procedures and precautions taken around these can
instill confidence in nominators that

##### Which regions nodes are in

A diverse network of nodes in varying different regions helps strengthen decentralized networks.
Outlining what regions nodes are in gives clarity to this facet of networks. Nominators may want to
promote validators that actively try and decentralize networks by region.

##### VPS / bare metal providers used

Outlining which providers are used for running nodes can help nominators get a sense of how
diversified a validator is. If every validator is hosted in AWS, there is a risk of potential
outages causes large amounts of nodes to go offline, causeing slashing for unresponsiveness.
Nominators may want to choose validators that have throuhoughly diversified the provider their nodes
are on.

##### Role based access control policies

Who has access to nodes?

##### Stake management automation

Is your own stake being utilized in the most efficient way possible? What tools are used to
determine how many nodes to run and how to

##### DDoS protection

##### Specs

Are you running the recommended Standard Hardware for Polkadot? Can you ensure that machines have
enough processing power, memory, file storage, and network connectivity? It's helpful for nominators
to know the specs of the machines a validator uses as to access how they may perform in the network.
If a validator is running underpowered machines, they may not want to nominate them, as these can
result in less blocks produced and less overall rewards.

### Communicating Well

Have direct channels of communication

### Actively Participating in the Community

Participating in the community goes hand in hand with building a reputation.

#### Participating in Governance

#### Producing Educational Content

While a lot of content

#### Building Tooling

Building public tooling is a great way to support the ecosystem. This not only provides tangible
value to those that use this tooling, but also gives visibility to the validator for their
contributions. A nominator might be more likely to nominate a validator for the utilities they
provide the ecosystem, since the validator then can build a reputation around the quality of their
work outside of their validatiion services. Some potential categories of building things are: block
explorers, deployment scripts, monitoring and observibility services, staking dashboards, wallets,
command line utilities, or porting implementations to other languages. Additionally, this may also
be eligable to be funded via a
[Web 3 Foundation Grant](https://github.com/w3f/General-Grants-Program).

[setting up a validator]: maintain-guides-how-to-validate-polkadot
[identity]: learn-identity#setting-an-identity

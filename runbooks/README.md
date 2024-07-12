# BNS V2 Runbooks

[![Txtx](https://img.shields.io/badge/Operated%20with-Txtx-gree?labelColor=gray)](https://txtx.sh)

## Runbooks available

#### Register BNS Name
Calls the `name-preorder` and `name-register` BNS V2 functions

#### Claim Preorder
This Runbook preorders a BNS name, then claims the preorder STX commitment

#### (Managed) Register BNS Name
Calls the `mng-name-preorder` and `mng-name-register` BNS V2 functions

#### Register BNS Namespace
Registers a BNS namespace

#### Update Zonefile Hash
Calls the update-zonefile-hash BNS V2 function, expecting the name to already be registered

## Getting Started

This repository is using [txtx](https://txtx.sh) for handling its on-chain operations.

`txtx` takes its inspiration from a battle tested devops best practice named `infrastructure as code`, that have transformed cloud architectures. 

`txtx` simplifies and streamlines Smart Contract Infrastructure management across blockchains, focusing on robustness, reproducibility and composability.

### Installation

```console
$ curl -sL https://install.txtx.sh/ | bash
```

### Scaffold a new runbook

```console
$ txtx new
```

Access tutorials and documentation at [docs.txtx.sh](https://docs.txtx.sh) to understand the syntax and discover the powerful features of txtx. 

Additionally, the [Visual Studio Code extension](https://marketplace.visualstudio.com/items?itemName=txtx.txtx) will make writing runbooks easier.

### List runbooks available in this repository
```console
$ txtx ls
ID                                      Name                                    Description
register-bns-name                       Register BNS Name                       Calls the name-preorder and name-register BNS V2 functions
claim-preorder                          Claim Preorder                          This Runbook preorders a BNS name, then claims the preorder STX commitment
mng-register-bns-name                   Register BNS Name                       Calls the mng-name-preorder and mng-name-register BNS V2 functions
namespace-register                      Register BNS Namespace                  Registers a BNS namespace
update-zonefile-hash                    Update Zonefile Hash                    Calls the update-zonefile-hash BNS V2 function, expecting the name to already be registered.
```

### Execute an Unsupervised Runbook
Unsupervised Runbooks will immediately execute all steps, signing transactions synchronously via mnemonic.
```console
$ txtx run namespace-register --unsupervised
```
### Execute a Supervised Runbook
Supervised Runbooks will allow a user to initiate each step of the Runbook, and allows browser wallet and mnemonic signing.
```console
$ txtx run claim-preorder
```

### Update the README documentation
```console
$ txtx docs --update 
```

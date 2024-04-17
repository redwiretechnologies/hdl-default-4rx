# hdl-default-4rx

This repository is designed to be an OOT module to use in conjunction with [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main).
It adds support for a version of our `default` project for a dual transceiver radio such as our Carbon SDR.

For issues with this repository, its documentation, or additional questions, please reach out to our lead FPGA engineer, Jonathan Ambrose, at (jambrose@redwiretechnologies.us).

---

# Requirements

This repository needs the requirements listed in the [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main) README.    

---

# Building

Please note that this repository only implements the personality, but it does not provide build targets as the Oxygen SDR does not support it.
To add build targets, please additionally use  [hdl-compat-default-4rx-carbon](https://github.com/redwiretechnologies/hdl-compat-default-4rx-carbon).   
 
To use this repository in conjunction with [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main), this repository must be checked out into the `oot` directory as shown below:
```
$ ls oot

hdl-default-4rx/
``` 

After having done this, you must run `scripts/link_oot.sh` from the [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main) repository. This will create hard symlinks from the files in your OOT modules to the directory structure within [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main).   

# Personalities

For clarification's sake on the nomenclature, a "personality" is a generic block diagram configuration that can/will be customized on a per board basis. A "project" is the single customized Vivado project for a combination of personality and board. 
 
## `default-4rx`

The `default-4rx` personality implements a version of our `default` project (described in the README of [hdl-rwt](https://github.com/redwiretechnologies/hdl-rwt/tree/main)) that supports a dual transceiver radio such as our Carbon SDR.

### Block Diagram


This block diagram uses the Carbon SDR as the intended platform.   

<center>


[![Block Diagram](images/bd/default-4rx.jpg)](images/bd/default-4rx.jpg)


</center>

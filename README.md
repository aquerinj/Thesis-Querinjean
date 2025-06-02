# Thesis – Designing a Cyber-Secure Infrastructure for Belgian SMEs (JANUS Adaptation)

This repository contains the code, documentation, and demonstration materials related to my Master's thesis:  
**"Designing a Cyber-Secure Infrastructure for Belgian SMEs: A Modular Approach aligned with the CyFun Framework, with Focus on the Accounting Sector"**


The complete infrastructure project is included as a compressed archive: JANUS.zip. A demonstration video and screenshots showing the infrastructure in action can be found in the demo/ folder.

## 📁 Project Structure

This is a copy of the original JANUS infrastructure, adapted and reorganized for academic and public use.

```

janus/
├── domain/
│   ├── user/                     # Main environment to launch (Vagrant)
│   └── cyfun/identify/           # CyFun Identify function scripts (AM-1 to RA-5)
│       ├── software/
│       ├── assets/
|       ├── inventory/
|       ├── checklist/            # checklist for each Cyfun sub-function
│       ├── information/
│       ├── policies/
│       ├── risk/
│       └── /*/output/               # Collected results
├── user/Vagrantfile
└── README.md

````

##  How to Launch the Project

###  Prerequisites (on Debian-based systems)

Install the required dependencies:

```bash
sudo apt update
sudo apt install virtualbox vagrant
````

###  Run the Project

Navigate to the user domain folder:

```bash
cd janus/domain/user
```

To launch the infrastructure:

```bash
vagrant destroy --force && vagrant box update && vagrant up
```

### ✅ Enable CyFun Compliance (asset inventory, vulnerability scans, etc.)

Before launching, set the following environment variable:

* On **Linux/macOS**:

```bash
USE_CYFUN=true vagrant destroy --force && vagrant box update && vagrant up
```

* On **Windows (CMD)**:

```cmd
set "USE_CYFUN=true" && vagrant destroy --force && vagrant box update && vagrant up
```

##  Demonstration

A screencast video and example outputs are available in the `/demo` folder or via the [GitHub repository](https://github.com/aquerinj/Thesis-Querinjean/demo).

## Purpose of This Work

This code demonstrates how SMEs, especially accounting firms, can:

* Automate inventory collection and documentation
* Reach CyFun Level Basic compliance for Identify (AM-1 to RA-5)
* Deploy isolated and reproducible infrastructure using Vagrant and Ansible

## License & Disclaimer

This repository is provided for educational and demonstration purposes.
The original JANUS codebase remains under the copyright of the
original authors at [https://gitlab.com/jdosec/janus](https://gitlab.com/jdosec/janus).

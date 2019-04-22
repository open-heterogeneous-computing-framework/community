# Open Heterogeneous Computing Framework (OHCF)
Open Source Full Stack Heterogeneous Computing Reference Framework

## Motivtation
Heterogeneous Computing (a.k.a domain specific accelerators such as GPU, FPGAs, SoCs, ASICs, etc) has started to play more and more important role in nascent technologies such as Artificial Intelligence, 5G, Edge Computing, Robotics, HPC, Blockchain and so forth, most of which is offered or ran via a cloud computing platform.

However heterogeneous computing, compared to CPU-oriented general computing which has mature ecosystem from hardware to software, is still in early stage and suffers from the lack of a rich ecosystem. Hardware vendors' software ecosystem world view rarely go beyond device SDK, whereas application developers just assume their software should run on any hardware. As a result cloud platform struggle to build the bridge to connect the two, as well as address the challeneges on the OS and virtualization/containerization level support.

Therefore an end-to-end full stack open source reference framework for heterogeneous computing is highly valuable, where people know how the domain specific accelerators are provided as a resource via cloud platform to the application, and how cloud platform could help applications to take advantages of these accelerator resources' perticular designs. 

Open Heterogeneous Computing Framework (OHCF) is proposed as a new open source initiative for this specific purpose. 

## Definition
### Overview
OHCF is a lightweight overlay project working with and across major upstream open source communities such as Linux Foundation, OpenStack Foundation, OCP Foundation, RISC-V Foundtion, etc. It is developer oriented and serves as a community for those are interested in accelerators to work together, build proof of concept implementations which could serve as a reference for users and vendors alike.

### Governance
OHCF is a developer oriented lightweight governed open source project, which means there will be no designated committees/boards/emeritus positions, at least in the early stage. The community will be spearheaded by those who are interested and excited about the heterogeneous computing open source implementations. Decisions will be driven by simple consensus from open discussion.

### Scope
OHCF aims to provide an open source reference framework for cloud computing powered hetergeneous computing implementations. [OpenStack](www.openstack.org) and [Kubernetes](www.kubernetes.io) will be the two main cloud computing platform OHCF's work will target. Non-cloud environment (simple single tenant clusters, blockchains) is non-priority or out of scope for OHCF.

### Goal/Deliverables
The main deliverables from OHCF will be reference framework in the format of either [PoC code](https://github.com/open-heterogeneous-computing-framework/PoC) or [design documentation](https://github.com/open-heterogeneous-computing-framework/Formula)

There will be also other types of deliverables (e.g open source [specifications](https://github.com/open-heterogeneous-computing-framework/Specs), or [open lab env](https://github.com/open-heterogeneous-computing-framework/Lab))

OHCF will however not produce integration release which would be too heavyweight. Most of the gap fulfilling features will go to respective upstream communities, and it is not the goal of OHCF to host forked major upstream implementations.

### Example Reference Framework
![Figure 1: Example Reference Framework Architecture](./example-arch.png "Figure 1: Example Reference Framework Architecture")

### Workflow
As shown in Figure 2 below, everything in OHCF starts with Formula.

Formula is where we gather or write up design blueprint of a full stack reference implementation of a certain scenario. For example one formula could be the design of how to run a machine learning inference job on a cloud platform powered by OpenStack and Kubernetes with FPGA resource. In thr formula the developer will specify what open source componenets would be needed, what upstream communities would be impacted, what are the versions of the software and hardware we will PoC on, and all the other informations.

The input for a formula design could be directly from an issue/PR, or from discussions happened in a OHCF related [conference](https://github.com/open-heterogeneous-computing-framework/conference).

After a formula is defined, there will be three options going forward: 

1) start PoC if there are no gaps identified; 

2) go to upstream communities if the gaps are straightforward;

3) write up a [HCIP](https://github.com/open-heterogeneous-computing-framework/HCIP) that describes the holistic requirements for improvements when the gaps are not easily defined.

When we go on the HCIP route, there will also be three outcomes of the HCIP process:

1) with clear defined gaps, go to the upstream communities to fulfill those gaps

2) Draft specification if needed

3) Build PoC which verifies the HCIP for follow up investigations

All the PoC could be materialized in an open lab environment.

![Figure 2: OHCF Workflow](./workflow.png "Figure 2: OHCF Workflow")

## Contribution
If you have any new idea about how we could better support accelerator ecosystem, feel free to submit an issue and start the conversation ! You could also asking question or provide ideas via the [OHCF google group](https://groups.google.com/forum/#!forum/ohcf), or join our [slack channel](https://join.slack.com/t/openheterogen-sua7347/shared_invite/enQtNjE0NjExNTI4NDgwLWY3ZWVmMDc1MGQzOGIyNjg2OWU0ZDExYWYyMmM5OGEzZDA0ZWNmYWZmZjg5NzRiYjljYTNmMGFiMDcxM2YxYmM)

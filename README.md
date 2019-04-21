# Formula
Reference Design Blueprint For Open Heterogeneous Computing Framework (OHCF)

## Motivtation
Heterogeneous Computing (a.k.a accelerators) has started to play more and more important role in nascent technologies such as Artificial Intelligence, 5G, Edge Computing, Robotics, HPC, Blockchain and so forth, most of which is offered or ran via a cloud computing framework.

However heterogeneous computing, compared to CPU-oriented general computing which has mature ecosystem from hardware to software, is still in early stage and suffers from the lack of ecosystem. Hardware vendors' software ecosystem world view rarely go beyond device SDK, whereas application developers just assume their software should run on any hardware. As a result cloud platform struggle to build the bridge to connect the two, as well as the challeneges on the OS and virtualization/containerization level support.

Therefore it would be great to have an end-to-end full stack open source reference framework for heterogeneous computing, where people know how the domain specific accelerators are provided as a resource via a certain cloud platform to the application, and how cloud platform could help applications to take advantages of these accelerator resources. 

Open Heterogeneous Computing Framework (OHCF) is proposed as a new open source initiative for this perticular purpose. 

## Definition and Scope
OHCF is a lightweight overlay project working with and across major upstream open source communities such as Linux Foundation, OpenStack Foundation, OCP Foundation, RISC-V Foundtion, etc. It is developer oriented and serves as a community for those are interested in accelerators to work together, build proof of concept implementations which could serve as a reference for users and vendors alike.

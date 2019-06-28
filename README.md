# OpenEBS

[![Build Status](https://img.shields.io/travis/openebs/openebs/master.svg?style=flat-square)](https://travis-ci.org/openebs/jiva)
[![Docker Pulls](https://img.shields.io/docker/pulls/openebs/jiva.svg?style=flat-square)](https://hub.docker.com/r/openebs/jiva/)
[![Releases](https://img.shields.io/github/release/openebs/openebs/all.svg?style=flat-square)](https://github.com/openebs/openebs/releases)
[![Slack](https://img.shields.io/badge/chat!!!-slack-ff1493.svg?style=flat-square)]( https://openebsslacksignup.herokuapp.com/)
[![Twitter](https://img.shields.io/twitter/follow/openebs.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=openebs)

http://www.openebs.io/
 
**OpenEBS** enables the use of containers for mission-critical, persistent workloads. OpenEBS is containerized storage and related storage services, sometimes called Container Attached Storage.  As of 2019 OpenEBS is a Cloud Native Computing Foundation project.  
 
**OpenEBS** allows you to treat your persistent workload containers, such as DBs on containers, just like other containers. OpenEBS itself is deployed as just another container on your host and enables storage services that can be designated on a per pod, application, cluster or container level, including:
- Data persistence across nodes, dramatically reducing time spent rebuilding Cassandra rings for example.
- Synchronization of data across availability zones and cloud providers.
- Use of commodity hardware plus a container engine to deliver so called container attached block storage.
- Integration with Kubernetes, so  developer and application intent flows into OpenEBS configurations automatically.
- Management of tiering to and from S3 and other targets.
  
**Our vision** is simple: let storage and storage services for persistent workloads be fully integrated into the environment and hence can be managed automatically that it almost disappears into the background as just yet another infrastructure service that just works. 

## Why OpenEBS Scales
 
OpenEBS can scale to include an arbitrarily large number of containerized storage controllers.  

## Installation and Getting Started
 
OpenEBS can be setup in few easy steps. You can get going on your choice of Kubernetes cluster by having open-iscsi installed on the Kubernetes nodes and running the openebs-operator using kubectl. 

**Start the OpenEBS Services using Operator**
```
wget https://raw.githubusercontent.com/openebs/openebs/master/k8s/openebs-operator.yaml
kubectl apply -f openebs-operator.yaml
```
**Customize or use the Default storageclasses**
```
wget https://raw.githubusercontent.com/openebs/openebs/master/k8s/openebs-storageclasses.yaml
kubectl apply -f openebs-storageclasses.yaml
```
You could also follow our [QuickStart Guide](https://docs.openebs.io/docs/overview.html).

OpenEBS can be deployed on any Kubernetes cluster - either in cloud, on-premise or developer laptop (minikube). Please follow our [OpenEBS Setup](https://docs.openebs.io/docs/overview.html) documentation. Also, we have a Vagrant environment available that includes a sample Kubernetes deployment and synthetic load that you can use to simulate the performance of OpenEBS. You may also find interesting the related project called Litmus (https://www.openebs.io/litmus) which helps with chaos engineering for stateful workloads on Kubernetes.  

## Status
We have reached OpenEBS 1.0! Please read more about 1.0 changes and vision here https://openebsblog.mayadata.io/openebs-announces-the-availability-of-version-1.0 
 
## Contributing
 
OpenEBS welcomes your feedback and contributions in any form possible.
 
- Join us at [Slack](https://openebsslacksignup.herokuapp.com/)
  - Already signed up? Head to our discussions at [#openebs-users](https://openebs-community.slack.com/messages/openebs-users/)
- Want to raise an issue?
  - If it is a generic (or `not really sure`), you can still raise it at [issues](https://github.com/openebs/openebs/issues)
  - Project (repository) specific issues also can be raised at [issues](https://github.com/openebs/openebs/issues) and tagged with the individual repository labels like *repo/maya*.
- Want to help with fixes and features?
  - See [open issues](https://github.com/openebs/openebs/labels)
  - See [contributing guide](./CONTRIBUTING.md)
  - Want to join our community, [check this out](./community/README.md). 

## Show me the Code

This is a meta-repository for OpenEBS. The source code is available at the following locations:
- The source code for the initial storage engine is under [openebs/jiva](https://github.com/openebs/jiva).
- The storage orchestration source code is under [openebs/maya](https://github.com/openebs/maya).
- While *jiva* and *maya* contain significant chunks of source code, some of the orchestration and automation code is also distributed in other repositories under the OpenEBS organization. 

Please start with the pinned repositories or with [OpenEBS Architecture](./contribute/design/README.md) document. 


## License

OpenEBS is developed under Apache 2.0 license at the project level. 
Some components of the project are derived from other open source projects like Nomad, Longhorn and are distributed under their respective licenses. 

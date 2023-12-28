<div style="text-align: center"></div>
  <p align="center">
  <img src="https://user-images.githubusercontent.com/42825450/225513881-67ffbdf1-dcda-495d-8c19-d0c6fd9eccc9.png" width="250px" height="220px">
      <br>
      <i>Deploying Highly Available Kubernetes Cluster using Binary Installation.</i>
  </p>
</div>


[![image](https://img.shields.io/badge/CNCF-Kubernetes-blue)](https://kubernetes.io/) 
[![image](https://img.shields.io/badge/%E5%AE%B9%E5%99%A8%E8%BF%90%E8%A1%8C%E6%97%B6-containerd-orange)](https://containerd.io/)
[![image](https://img.shields.io/badge/%E5%AE%B9%E5%99%A8%E8%BF%90%E8%A1%8C%E6%97%B6-Docker-brightgreen)](https://www.docker.com/) 
[![image](https://img.shields.io/badge/%E5%88%86%E5%B8%83%E5%BC%8FKV%E5%AD%98%E5%82%A8%E7%B3%BB%E7%BB%9F-ETCD-orange)](https://etcd.io/)
[![image](https://img.shields.io/badge/TCL-CFSSL-%2320a0ff)](https://github.com/cloudflare/cfssl)
[![image](https://img.shields.io/badge/Network-Calico-%23f68245)](https://github.com/projectcalico/calico)
> 跟着本文档带你通过原始二进制方式，从0到1部署一套完整的、高可用、生产可用的K8s集群<br>
> Follow this document to deploy a complete, highly available, production-ready K8s cluster from scratch using the raw binary approach, from 0 to 1. <br>

&nbsp; &nbsp; *[View My Blog](https://www.dqzboy.com/)*
<br />

<div align="center">
 
[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Handlee&center=true&vCenter=true&width=500&height=60&lines=Deploying+Highly+Available+Kubernetes+Cluster)](https://git.io/typing-svg)
 
<img src="https://camo.githubusercontent.com/82291b0fe831bfc6781e07fc5090cbd0a8b912bb8b8d4fec0696c881834f81ac/68747470733a2f2f70726f626f742e6d656469612f394575424971676170492e676966"
width="800"  height="3">
</div>

## 部署说明 | deployment instructions
目前本文档是基于K8s 1.25 版本进行部署和更新梳理，如果你部署是其他K8s版本，请阅读K8s的版本[更新日志](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.25.md)，确保与本文档中组件所使用的参数可以在你所部署的版本之上运行！<br>
Currently, this document is based on the deployment and update process using K8s version 1.25. If you are deploying with a different K8s version, please refer to the version update log of K8s to ensure that the parameters used by the components in this document can operate on the version you are deploying!

## 第一章：角色分配划分 | Chapter 1: Role Assignment and Division
- [一、角色规划和分配 | 一、Role Planning and Assignment ](deploydoc/一、角色规划和分配.md)


## 第二章：系统初始化 | Chapter 2: System Initialization
- [二、系统初始化 | 二、system initialization ](deploydoc/二、系统初始化.md)


## 第三章：CA根证书创建 | Chapter 3: CA Root Certificate Creation
- [三、创建CA根证书和秘钥 | 三、Create CA root certificate and secret key ](deploydoc/三、创建CA根证书和秘钥.md)


## 第四章：部署ETCD集群 | Chapter 4: Deploying an etcd cluster
- [四、部署ETCD集群 | 四、Deploying an etcd cluster ](deploydoc/四、部署ETCD集群.md)


## 第五章：部署kubectl命令行工具 | Chapter 5: Deploying the kubectl command-line tool
- [五、部署kubectl命令行工具 | 五、Deploying the kubectl command-line tool ](deploydoc/五、部署kubectl命令行工具.md)


## 第六章：部署Master节点 | Chapter 6: Deploying the Master Node
- [六、部署Master节点 | 六、Deploying the Master Node ](deploydoc/六、部署Master节点)
  - [1、部署环境说明 | 1、Deployment environment description ](deploydoc/六、部署Master节点/1、部署环境说明.md)
  - [2、集群节点高可用访问kube-apiserver | 2、Highly available access to the kube-apiserver from resource nodes. ](deploydoc/六、部署Master节点/2、集群节点高可用访问kube-apiserver.md)
  - [3、部署高可用kube-apiserver集群 | 3、Deploy a high-availability kube-apiserver cluster. ](deploydoc/六、部署Master节点/3、部署高可用kube-apiserver集群.md)
  - [4、部署高可用kube-controller-manager集群 | 4、Deploy a high-availability kube-controller-manager cluster. ](deploydoc/六、部署Master节点/4、部署高可用kube-controller-manager集群.md)
  - [5、部署高可用kube-scheduler 集群 | 5、Deploy a high-availability kube-scheduler cluster. ](deploydoc/六、部署Master节点/5、部署高可用kube-scheduler集群.md)

## 第七章：部署Worker节点 | Deploy Worker Nodes
- [七、部署Worker节点 | 七、Deploy Worker Nodes ](deploydoc/七、部署Worker节点)
  - [1、部署环境说明 | 1、Deployment Environment Description ](deploydoc/七、部署Worker节点/1、部署环境说明.md)
  - [2、部署containerd |2、Deploy containerd](deploydoc/七、部署Worker节点/2、部署containerd.md)
  - [3、部署kubelet组件 | 3、Deploy kubelet Component ](deploydoc/七、部署Worker节点/3、部署kubelet组件.md)
  - [4、部署kube-proxy组件 | 4、Deploy kube-proxy Component ](deploydoc/七、部署Worker节点/4、部署kube-proxy组件.md)
  - [部署docker运行时(仅作参考) ](deploydoc/七、部署Worker节点/部署docker运行时(仅作参考).md)

## 第八章：部署网络插件
- [八、部署网络插件 ](deploydoc/八、部署网络插件)
  -  [部署网络插件 ](deploydoc/八、部署网络插件/八、部署网络插件.md)
  -  [部署Cilium替代kube-proxy ](deploydoc/八、部署网络插件/部署Cilium替代kube-proxy.md)

## 九、验证集群状态
- [九、验证集群状态 ](deploydoc/九、验证集群状态)
  -  [验证集群状态 ](deploydoc/九、验证集群状态/验证集群状态.md)

## 十、部署集群插件
- [十、部署集群插件 ](deploydoc/十、部署集群插件)
  -  [1、部署Coredns插件 ](deploydoc/十、部署集群插件/1、部署Coredns插件.md)
  -  [2、部署 Dashboard 插件 ](deploydoc/十、部署集群插件/2、部署Dashboard插件.md)

## 说明
本专题仅供学习和交流使用，请勿用于商业用途，并在转载时注明本专题地址。<br>
由于本人水平有限，文中可能存在遗漏或错误之处，敬请指正并不吝赐教，感激不尽。<br>

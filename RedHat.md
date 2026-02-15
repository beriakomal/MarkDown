# Chapter 1. OpenShift Container Platform installation overview
## 1.1. About OpenShift Container Platform installation

The OpenShift Container Platform installation program offers four methods for deploying a cluster which are detailed in the following list:

* **Interactive:** You can deploy a cluster with the web-based [Assisted Installer](https://docs.redhat.com/en/documentation/assisted_installer_for_openshift_container_platform/2026). This is an ideal approach for clusters with networks connected to the internet. The Assisted Installer is the easiest way to install OpenShift Container Platform, it provides smart defaults, and it performs pre-flight validations before installing the cluster. It also provides a RESTful API for automation and advanced configuration scenarios.
* **Local Agent-based:** You can deploy a cluster locally with the [Agent-based Installer](https://console.redhat.com/openshift/install/metal/agent-based) for disconnected environments or restricted networks. It provides many of the benefits of the Assisted Installer, but you must download and configure the Agent-based Installer first. Configuration is done with a command-line interface. This approach is ideal for disconnected environments.
  * Additionally, you can deploy a cluster without an external registry, using self-contained installation media that also provides a simplified user interface similar to the Assisted Installer during on-premise installations. For more information, see "Installing a cluster without an external registry".

### 1.1.1. About the installation program 

You can use the installation program to deploy each type of cluster. The installation program generates the main assets, such as Ignition config files for the bootstrap, control plane, and compute machines. You can start an OpenShift Container Platform cluster with these three machine configurations, provided you correctly configured the infrastructure.

The OpenShift Container Platform installation program uses a set of targets and dependencies to manage cluster installations. The installation program has a set of targets that it must achieve, and each target has a set of dependencies. Because each target is only concerned with its own dependencies, the installation program can act to achieve multiple targets in parallel with the ultimate target being a running cluster. The installation program recognizes and uses existing components instead of running commands to create them again because the program meets the dependencies.

![Image](/Images/targets-and-dependencies.png)

### 1.1.2. About Red Hat Enterprise Linux CoreOS (RHCOS) 
Post-installation, each cluster machine uses Red Hat Enterprise Linux CoreOS (RHCOS) as the operating system. RHCOS is the immutable container host version of Red Hat Enterprise Linux (RHEL) and features a RHEL kernel with SELinux enabled by default. RHCOS includes the `kubelet`, which is the Kubernetes node agent, and the CRI-O container runtime, which is optimized for Kubernetes. 
>**Note:** You cannot modify the parameters that you set during installation, but you can modify many cluster attributes after installation.

<style>
table, th, td {
  border: 1px solid black;
}
</style>
<table>
  <tr>
    <th>Platform</th>
    <th>Installer-provisioned infrastructure[1]</th>
    <th>Installer-provisioned infrastructure[2]</th>
    <th>Agent-based Installer</th>
  </tr>
  <tr>
    <td>Amazon Web Services (AWS)</td>
    <td>X</td>
    <td>X</td>
    <td></td>
  </tr>
  <tr>
    <td>Bare Metal</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
  </tr>
</table>
# Baiju's Helm Project Notes

This repository contains personal notes related to my Helm project-related
works.  My [office job][office-job] also has few Helm project-related works.  I
am still learning about the Helm project.  This repository helps me to track my
work. But if you have any feedback, please send a mail to my email address:
baiju.m.mail AT gmail.com.

## Pull Requests

1. https://github.com/helm/helm-www/pull/928 (My first PR. It took more than 6 months to merge!)
1. https://github.com/helm/helm/pull/9750

Apart from the above pull requests, I started [pull requests
review](https://github.com/helm/helm/pulls?q=reviewed-by:baijum) recently.


## Side Projects

1. https://github.com/baijum/helm-cluster-repo


## Ideas

1. What would be required to support release channels for helm charts?  In
   addition to the chart version, an [Application
   Distributor][application-distributor] should be able to set the release
   channel.  The release channel information can be captured as annotation in
   the `index.yaml` entry for the chart.  If the idea seems to get more
   acceptance, it can be promoted as a distinct attribute itself.  Examples:

   ```
   releaseChannel: alpha
   releaseChannel: beta
   releaseChannel: stable
   ```

   Until the Helm client recognizes these values, a plugin can be used to
   install helm charts from a given channel.

   ```
   helm channel-install my-chart example/chart --channel beta
   helm channel-install my-chart example/chart --version 0.2.0 --channel alpha
   ```

## Resources

1. [User
	profiles](https://github.com/helm/community/blob/main/user-profiles.md): The
	purpose of this document is to aid in the development of Helm features by
	evaluating Helm features against those who will be using them.


## To Read

### Package Managers, Dependency Analysis, Update Process etc.

I want to understand the big picture and familiarise what's in use in the
industry.  I will be slowly exploring other projects and industry standards in
the coming months.

This list is not in a particular order:

1. https://ostreedev.github.io/ostree/
1. https://github.com/rpm-software-management/dnf
1. https://github.com/operator-framework/operator-lifecycle-manager
1. https://wiki.debian.org/PackageManagement
1. https://guix.gnu.org/ & https://nixos.org/
1. https://fuchsia.dev/fuchsia-src/concepts/packages/package
1. https://www.pypa.io/en/latest/
1. http://tug.org/texlive/pkgcontrib.html & https://www.ctan.org/file/help/ctan/CTAN-upload-addendum
1. https://www.freedesktop.org/wiki/ApplicationPackageSpec/
1. https://golang.org/doc/modules/developing
1. https://docs.npmjs.com/packages-and-modules
1. https://theupdateframework.io

### Interesting Projects

1. https://github.com/theupdateframework/notary

### Articles

1. https://kubernetes.io/docs/tutorials/kubernetes-basics/update/update-intro/
1. https://kubernetes.io/docs/concepts/workloads/controllers/deployment/

[office-job]: https://github.com/openshift-helm-charts/charts
[application-distributor]: https://github.com/helm/community/blob/main/user-profiles.md#2-application-distributor

---
title: jx gitops repository resolve
linktitle: resolve
type: docs
description: "Resolves the git repository URL for the cluster/environment"
aliases:
  - jx-gitops_repository_resolve
---

### Usage

```
jx gitops repository resolve
```

### Synopsis

Resolves the git repository URL for the cluster/environment

### Examples

  ```bash
  # updates git repository URL for the resources in the current directory
  jx-gitops repository resolve https://github.com/myorg/myrepo.git
  # updates git repository URL for the resources in some directory
  jx-gitops repository resolve --dir something https://github.com/myorg/myrepo.git

  ```
### Options

```
  -d, --dir string                the directory look for the 'jx-requirements.yml` file (default ".")
  -h, --help                      help for resolve
      --invert-selector           inverts the effect of selector to exclude resources matched by selector
  -k, --kind stringArray          adds Kubernetes resource kinds to filter on. For kind expressions see: https://github.com/jenkins-x/jx-helpers/v3/tree/master/docs/kind_filters.md
      --kind-ignore stringArray   adds Kubernetes resource kinds to exclude. For kind expressions see: https://github.com/jenkins-x/jx-helpers/v3/tree/master/docs/kind_filters.md
      --selector stringToString   adds Kubernetes label selector to filter on, e.g. -s app=pusher-wave,heritage=Helm (default [])
      --selector-target string    sets which path in the Kubernetes resources to select on instead of metadata.labels.
  -s, --source-dir string         the directory to recursively look for the *.yaml or *.yml source Environment/SourceRepository files (default ".")
```



### Source

[jenkins-x-plugins/jx-gitops](https://github.com/jenkins-x-plugins/jx-gitops)

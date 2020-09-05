---
author: Naoki Oketani
title: Files that should be updated in `dev-1.18-ja.2`
date: 2020-09-05
description: A brief guide to setup KaTeX
tags:
- kubernetes-docs-ja
---

We are now updating Kubernetes docs Japanese version in `dev-1.18-ja.1`.
After that, the documents should be updated to follow [v1.18 English version](https://v1-18.docs.kubernetes.io/docs/home/).

```bash
for f in $(git ls-files -z content/ja/docs/ \
  | xargs -0 -n1 -I{} -- git log -1 --format="%ai {}" {} \
  | awk '{print $4}' \
  | sed -e 's/ja/en/'); \
do git diff --name-only fb6364d upstream/release-1.18 -- $f; done
| sed -e 's#/en/#/ja/#'
```

The output is as below.

```
content/ja/docs/_index.md
content/ja/docs/concepts/architecture/controller.md
content/ja/docs/concepts/architecture/nodes.md
content/ja/docs/concepts/configuration/manage-resources-containers.md
content/ja/docs/concepts/configuration/secret.md
content/ja/docs/concepts/containers/container-lifecycle-hooks.md
content/ja/docs/concepts/extend-kubernetes/operator.md
content/ja/docs/concepts/storage/persistent-volumes.md
content/ja/docs/concepts/workloads/controllers/deployment.md
content/ja/docs/concepts/workloads/pods/pod-lifecycle.md
content/ja/docs/home/supported-doc-versions.md
content/ja/docs/reference/access-authn-authz/authentication.md
content/ja/docs/reference/glossary/kube-apiserver.md
content/ja/docs/reference/kubectl/cheatsheet.md
content/ja/docs/setup/production-environment/container-runtimes.md
content/ja/docs/setup/release/version-skew-policy.md
content/ja/docs/tasks/configure-pod-container/quality-service-pod.md
content/ja/docs/tutorials/_index.md
content/ja/docs/tutorials/kubernetes-basics/explore/explore-intro.html
content/ja/docs/tutorials/services/source-ip.md
```
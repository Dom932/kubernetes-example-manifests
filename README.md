# Kubernetes Example Manifests

This repository contains a number of example Kubernetes manifest files (currently targeting k8s version 1.19 and above) that follow security best practise that can be used as a template for your manifest files.

Currently this repository offers its examples in two forms of templates:

* Static YAML manifest template
* Kustomize configuration manager template

These example/templates should be used as a reference only and will require modification to fit your use cases.

Each example/template is currently scanned via following security and best practice analysers:

* [checkov](https://github.com/bridgecrewio/checkov)
* [kube-lint](https://github.com/stackrox/kube-linter)

## Kustomize

Kustomize is a configuration management tool for Kubernetes manifest files (much like helm) and is built into `kubectl` via the use of `kubectl apply -k` command.  Currently all static manifest files are generated from the Kustomize templates.

### Example command to build manifest using Kustomize

```bash
kustomize build --load-restrictor LoadRestrictionsNone ./kustomize-templates/best-practice-deployment/ > output.yml
 ```

## Future Improvements

* Add documentation/explanation to each setting.
* Include more examples/templates
* Include Helm examples

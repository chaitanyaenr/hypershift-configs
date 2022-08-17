## Conformance


Conformance runs the end-to-end test suite to check the sanity of the OpenShift cluster.

Assuming that the podman is installed, conformance/e2e test can be run using the following command:
```
$ podman run --privileged=true --name=conformance -d -v <path-to-kubeconfig>:/root/.kube/config quay.io/openshift-scale/conformance:latest
$ podman logs -f conformance
```

NOTE: source dockerfile for the image is [here](https://github.com/openshift-scale/scale-ci-diagnosis/blob/master/containers/conformance/Dockerfile)

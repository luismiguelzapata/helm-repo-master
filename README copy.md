# helm-umbrella-master# helm-tutorial
helm Chart examples and tutorial resources

This is an example charts repository.

### On ArgoCD
1) Create the namespaces of the projects
2) Apply the appProject.yaml

### Updated Chart.-
1) Update the version of the Chart.yaml when modify any repository files.
2) Proceed like the following steps




```console
$ cd helm-repo-master
$ (If not exist) mkdir docs
$ helm package . 
$ mv mv helm-repo-master-*.tgz docs
$ helm repo index docs --url https://luismiguelzapata.github.io/helm-repo-master
$ git add --all
$ git commit -am "Updated to version Release Version "
$ git push 
```

From there, I can do a `helm repo add helm-repo-master https://luismiguelzapata.github.io/helm-repo-master`


### Running
```console
$ kubectl apply helm-app-01/argocd/applicationset.yaml
```

### Building using Library: (NO lo uso)
```
$ helm package library-chart 
$ helm dependency build nginx-chart
$ helm template nginx-chart nginx-chart
$ helm package nginx-chart
```

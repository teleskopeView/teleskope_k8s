# teleskope_k8s

## Reasoning

When using `flux` our pipelines, or to be more precise, our Continues Deployments are fully automated and that's great.
But, sometimes we would like to have more stable environments with fewer deployments and with more control, for example, production.
That's mean we need to do some manual actions against `flux` which have his own CLI tool `fluxctl`.

flux-web is intended to be the UI approach to this problem. With flux-web we can view at our workloads per namespace with their available versions and with a single click we can promote a workload or to perform a rollback.

## Getting Started

The easiset way to deploy flux-web is with helm:
```shell
git clone git@github.com:flux-web/flux-web.git
cd flux-web/chart/flux-web
kubectl create ns flux
helm install . --name flux-web \
               --set namespace=flux
```
Or, for an example we can deploy flux-web as readonly mode:
```shell
helm install . --name  \
               --set namespace=flux
               --set frontend.env.READ_ONLY=true
```

Deploying teleskope with `HelmRelease`:
```
---

```

## Continued Development

Basically a roadmap.

### Coming soon


### Maybe in the future, if people want it

- user access and authentication

### Probably in the future

- select and release multiple workloads

## Built With

* [beego](https://beego.me/) - Backend framework
* [go](https://golang.org/) - Programing language
* [vue.js](https://vuejs.org/) - Frontend framework
* [nuxt.js](https://nuxtjs.org/) - Giving vue.js the ability to do ssr
* [docker](https://www.docker.com/) - Containerized with docker
* [helm](https://www.helm.sh/) - Packaged with helm


## Contributing

Code contributions are very welcome. If you are interested in helping make flux-web great then feel free!

## Authors 

* [Ido Braunstain](https://github.com/idobry) - *Initial work*
* [Efrat Lavitan](https://github.com/efrat19) - *Initial work*

Terraform Provider
==================

- Website: https://www.terraform.io
- [![Gitter chat](https://badges.gitter.im/hashicorp-terraform/Lobby.png)](https://gitter.im/hashicorp-terraform/Lobby)
- Mailing list: [Google Groups](http://groups.google.com/group/terraform-tool)

<img src="https://cdn.rawgit.com/hashicorp/terraform-website/master/content/source/assets/images/logo-hashicorp.svg" width="600px">

Maintainers
-----------

Jeff Gensler (@jeffzzq)

Requirements
------------

-	[Terraform](https://www.terraform.io/downloads.html) 0.10.x
-	[Go](https://golang.org/doc/install) 1.8 (to build the provider plugin)

Usage
---------------------

```
# For example, restrict template version in 0.1.x
provider "minikube" {
  version = "~> 0.1"
}
```

Building and Testing The Provider
---------------------

You will need `glide` and `gpgme` installed.

```
brew install glide
brew install gpgme
```

```bash
# Build
go get github.com/jgensler8/terraform-provider-minikube
glide install [--strip-vendor]
go build -o example/plugins/terraform-provider-minikube
# Test
cd example
terraform plan
```

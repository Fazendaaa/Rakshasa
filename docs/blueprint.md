{{ template:title }}

{{ template:logo }}

{{ template:badges }}

{{ template:description }}

Welcome to Fazendaaa's {{ pkg.name }}. This is version {{ pkg.version }}!

Made with:

- [Go](https://golang.org/)
- [Docker](https://www.docker.com/)

## Ideia

Currently, in the company that I work for we have a CLI (Command Line Interface) made in [Python](https://www.python.org/) called `estat` that you can read more about it right [here](https://github.com/Fazendaaa/Succubus). {{ pkg.name }} by itself ain't a reimplemented version of a current `estat` feature, but a new one; as some may know, there are many Continuos Integration (CI) / Continouos Delivery (CD) platforms as:

- [Github Actions](https://github.com/features/actions)
- [Circle CI](https://circleci.com/)
- [Gitlab's CI/CD](https://docs.gitlab.com/ee/ci/)
- [Travis CI](https://travis-ci.org/)
- [Jenkins](https://www.jenkins.io/)
- etc.

And many of those services have their own way of doing this, which becomes a pain when migrating from one to another or even updating something.

The idea is to have something like a `raksh.yaml` looking like:

```yaml
version: '1'

ci:
  image: registry/user/repo
  install:
    - <setup comand one>
    - <setup comand two>
    - <setup comand three>
    - ...
  test:
    - ...
  linter:
    - ...

cd:
  image: registry/user/repo
  docs:
    - ...
  k8s:
    - ...
```

As `estat` have grown so much and making it available as FOSS (Free and open-source software) was always the idea but the project still in development and not having a properly defined scope, I decided to break its main features in other projects:

- [Succubus](https://github.com/Fazendaaa/Succubus): universal package manager based on cloud-native
- [Jinn](https://github.com/Fazendaaa/Jinn): universal project manager built to expand Succubus capabilities
- [Baba Yaga](https://github.com/Fazendaaa/BabaYaga): universal cloud-native manager built to expand Jinn and Succubus capabilities
- [Rakshasa](https://github.com/Fazendaaa/Rakshasa): universal project translator from cloud-native projects to other infra technologies
- [Shōjō](https://github.com/Fazendaaa/): LaTex package manager
- [Hellhound](https://github.com/Fazendaaa/Hellhound): VSCode extension to integrate Jinn recipes
- [Crocotta](https://github.com/Fazendaaa/Crocotta): SOC assisted guider
- [Changeling](https://github.com/Fazendaaa/Changeling): Recipes for Succubus and Baba Yaga
- [Rakshasa](https://github.com/Fazendaaa/Rakshasa): CI/CD translator

## Components

### port

```shell
wend port
```

## Installing

You don't need to install Go to run this tool, just Docker. And to do so to give it a try, you can do it just by running the following line in your terminal:

```shell
alias wend='docker run -it --volume $(pwd):/project --workdir /project fazenda/Rakshasa'
```

And then running the following to check whether or not is working properly:

```shell
wend --help
```

## Running

## Author

Only [me](https://github.com/Fazendaaa) because the aforementioned project was implemented by yours only. By knowing each line of that code wrote doing the port would be more easily done this way.

## Contributing

Check more about this in [CONTRIBUTING.md](CONTRIBUTING.md). Here we have a list of some of our contributors:

{{ template:contributors }}

## TODO

## References

{{ template:license }}

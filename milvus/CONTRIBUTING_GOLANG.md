# How to contribute to Golang?

Before you make any contributions to Milvus, you should have a concept of our [Github workflow](CONTRIBUTING.md#github-workflow)

## How to build from source?

See [Building Milvus on a local OS/shell environment](DEVELOPMENT.md#building-milvus-on-a-local-osshell-environment),  make sure your environment meets the hardware and software requirements.

Build Milvus with:

```shell
milvus$ make milvus
```

> `milvus$` means we are in shell environment and at the root path of milvus repository directory.

## Coding style guidelines

Milvus values good coding style following [Effective GO](golang.org/doc/effective_go), [uber-go guide](https://github.com/uber-go/guide).

Apart from `gofmt`, we also use `golangci-lint` and `ruleguard` to do static checks.

To make sure your codes meet our coding style, you can check them locally.

```shell
milvus$ make fmt # gofmt check
```

Install check dependences, and run `golangci-lint` and `ruleguard` check

```shell
milvus$ make getdeps
milvus$ make static-check # golangci-lint check, see .golangci.yml for details.
milvus$ make ruleguard # ruleguard check, see ruleguard.rules.go for details.
```

Or you can check them all-together

```shell
milvus$ make verifiers # gofmt, golangci-lint, ruleguard and cppcheck all together
```

## How to run unit tests?

Milvus contains 3 types of tests, unit tests, integration tests and end-to-end tests. See [Testing](https://milvus.io/community/contributing_to_milvus.md#Testing) for details.

While contributing to Milvus,

- For bug fixes and improvements, unit tests are the ones to  pay attention. Every PR needs to pass all unit tests before merging into the master branch.
- For enhancements, apart from unit tests, you also need to pay attention to the integration tests. 

To run unit tests of Golang, you need to start the third-party services first.

```shell
milvus$ docker-compose -f deployments/docker/dev/docker-compose.yml up -d 
```

Then run all the tests.

```shell
milvus$ make test-go
```

You can also test each package individually. For example, if you want to run unit tests in `datanode` package. 

```shell
milvus$ cd internal/datanode
milvus/internal/datanode$ go test . -race -cover
```

See [Go testing package doc](https://pkg.go.dev/testing#hdr-Subtests_and_Sub_benchmarks)  for how to run subtests.

After the tests, don't forget to stop those third-party services.

```shell
milvus$ docker-compose -f deployments/docker/dev/docker-compose.yml down
```


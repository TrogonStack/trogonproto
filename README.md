# trogonproto

**trogonproto is the Go bindings module for the [trogon-proto](https://github.com/TrogonStack/trogon-proto) contract.**

**trogonproto exposes the generated Go types for every schema defined in `trogon-proto` — errors, env vars, UUIDs, consistency, streams, relay pagination, and more.** It tracks each release of the upstream proto module and ships pre-compiled `.pb.go` files under a stable import prefix so consumers never need to run `protoc` or `buf` themselves. Importing a contract is the same as importing any other Go package.

**trogonproto removes the toolchain burden that usually comes with adopting a shared protobuf contract in Go.** Without it, every service has to install `buf`, wire up codegen into its build, and keep generated output in sync with the proto repo on every bump — work that has nothing to do with the service itself and that drifts the moment one team forgets to regenerate.

**trogonproto is useful for any Go service, library, or tool that consumes the TrogonStack contracts.** Service teams pick up new fields by `go get`-bumping a single dependency. Library authors (e.g. `trogonerror`) can rely on stable Go types for the contract without taking a transitive dependency on the protobuf toolchain. Platform teams get a single place to publish, version, and audit the Go-facing surface of every TrogonStack proto.

An example to help Brex setup with EngFlow.
The content is copied from the public [EngFlow Example repo.](https://github.com/EngFlow/example/),
and contains platforms and toolchains for enabling Host:Mac, Exec: Linux

To use, copy the content of `brex_example/.bazelrc` into your `.bazelrc`, and copy over the entire `remote_config` directory into your repo. Then build a target using `--config=brex`.

Note: In `.bazelrc`, change `--tls_client_key` and `--tls_client_certificate` to the paths to those files on your machine.

Example invocation in this repo:
```
bazel build //genrules/... --config=brex
```

```
./bazel5.2.0_persistent run //java/com/engflow/example:example_bin --config=brex --config=mac --noremote_accept_cached
```


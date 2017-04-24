# ex_datadog_plug

A plug for logging response time in datadog. To use it, just plug it into the desired module:

```elixir
# ...
plug Plug.RequestId
plug ExDatadog.Plug, prefix: "your-service", method: true, query: []
# ...
```

## Options

* `:prefix` - the prefix you want to put for this stat. Default is `plug`.
* `:method` - a boolean value to include the method in the tag list. Default is `false`.
* `:query` - a list of strings to include specific query string in the tag list. `[]` will generate all query params as tags. Default is `nil` (do not generate tag for query string)

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `ex_datadog_plug` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [{:ex_datadog_plug, "~> 0.1.0"}]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/ex_datadog_plug](https://hexdocs.pm/ex_datadog_plug).

# RedixCluster

A wrapper around Redix that allows you to connect to a Redis cluster.

## Installation

1. Add redix_cluster to your list of dependencies in `mix.exs`:
```elixir
  def deps do
    [{:redix_cluster_remastered, "~> 1.0.0"}]
  end
```

2. Ensure redix_cluster is started before your application:
```elixir
def application do
  [applications: [:redix_cluster_remastered]]
end
```

## Sample Config

```elixir
config :redix_cluster_remastered,
  cluster_nodes: [
    %{host: "localhost", port: 6379}
  ],
  pool_size: 5,
  pool_max_overflow: 0
```
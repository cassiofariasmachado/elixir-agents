# Elixir agents

Notes about Elixir agents.

## Creating a agent

```elixir
{:ok, agent} = Agent.start_link fn -> %{} end
```

## Checking if agent is alive

```elixir
Process.alive?(agent)
```

## Update the value of the agent

```elixir
Agent.update(agent, fn my_map -> Map.put(my_map, :fruta, "banana") end)
```

## Getting the value of the agent 

```elixir
Agent.get(pid, fn my_map -> IO.inspect(my_map) end)
``` 
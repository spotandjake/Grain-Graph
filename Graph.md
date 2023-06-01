---
title: Graph
---

A library for weighted directed graphs.

## Types

Type declarations included in the Graph module.

### Graph.**Graph**

```grain
record Graph {
  graphStore: Map.Map<String, Map.Map<String, Number>>,
}
```

The Internal Representation Of The Graph

## Values

Functions and constants included in the Graph module.

### Graph.**make**

```grain
make : () -> Graph
```

Creates a new empty Graph.

Returns:

|type|description|
|----|-----------|
|`Graph`|A new empty Graph|

### Graph.**size**

```grain
size : (graph: Graph) -> Number
```

Determines the number of vertex's in a given graph.

Parameters:

|param|type|description|
|-----|----|-----------|
|`graph`|`Graph`|The given graph|

Returns:

|type|description|
|----|-----------|
|`Number`|The size of the given graph|

### Graph.**sizeNeighbors**

```grain
sizeNeighbors : (vertex: String, graph: Graph) -> Number
```

Determines the number of edges for a given vertex.

Parameters:

|param|type|description|
|-----|----|-----------|
|`vertex`|`String`|The given vertex|
|`graph`|`Graph`|The given graph|

Returns:

|type|description|
|----|-----------|
|`Number`|The size of the given vertex|

### Graph.**hasVertex**

```grain
hasVertex : (vertex: String, graph: Graph) -> Bool
```

### Graph.**addVertex**

```grain
addVertex : (vertex: String, graph: Graph) -> Void
```

### Graph.**removeVertex**

```grain
removeVertex : (vertex: String, graph: Graph) -> Void
```

### Graph.**hasEdge**

```grain
hasEdge : (vertex: String, neighbor: String, graph: Graph) -> Bool
```

### Graph.**addEdge**

```grain
addEdge :
  (vertex: String, neighbor: String, weight: Number, graph: Graph) -> Void
```

### Graph.**getWeight**

```grain
getWeight :
  (vertex: String, neighbor: String, weight: a, graph: Graph) ->
   Option<Number>
```

### Graph.**setWeight**

```grain
setWeight :
  (vertex: String, neighbor: String, weight: Number, graph: Graph) -> Void
```


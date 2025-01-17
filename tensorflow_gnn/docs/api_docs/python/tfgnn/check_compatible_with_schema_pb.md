# tfgnn.check_compatible_with_schema_pb

[TOC]

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api nocontent" align="left">
<td>
  <a target="_blank" href="https://github.com/tensorflow/gnn/tree/master/tensorflow_gnn/graph/schema_utils.py#L188-L227">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td>
</table>

Checks that the given spec or value is compatible with the graph schema.

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>tfgnn.check_compatible_with_schema_pb(
    graph: Union[<a href="../tfgnn/GraphTensor.md"><code>tfgnn.GraphTensor</code></a>, <a href="../tfgnn/GraphTensorSpec.md"><code>tfgnn.GraphTensorSpec</code></a>],
    schema: <a href="../tfgnn/GraphSchema.md"><code>tfgnn.GraphSchema</code></a>
) -> None
</code></pre>

<!-- Placeholder for "Used in" -->

The `graph` is compatible with the `schema` if

*   it is scalar (rank=0) graph tensor;
*   has single graph component;
*   has matching sets of nodes and edges;
*   has matching sets of features on all node sets, edge sets, and the context,
    and their types and shapes are compatible;
*   all adjacencies are of type
    <a href="../tfgnn/Adjacency.md"><code>tfgnn.Adjacency</code></a>.

<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Args</h2></th></tr>

<tr>
<td>
`graph`<a id="graph"></a>
</td>
<td>
The graph tensor or graph tensor spec.
</td>
</tr><tr>
<td>
`schema`<a id="schema"></a>
</td>
<td>
The graph schema.
</td>
</tr>
</table>

<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Raises</h2></th></tr>

<tr>
<td>
`ValueError`<a id="ValueError"></a>
</td>
<td>
if `spec_or_value` is not represented by the graph schema.
</td>
</tr>
</table>

# Network.r

<script type="text/javascript" src="../js/general.js"></script>

* calculate a new network while removing several nodes and their linking nodes recursively (當移除數個啟始節點與遞迴移除其相連的其他節點所形成的網路)

```R
matrix networkAfterRemoveNodes(
  matrix originNetwork, 
  vector selectedNodes, 
  bool isDirected
)
```
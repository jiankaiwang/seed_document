# seedalgorithm.h

<script type="text/javascript" src="../js/general.js"></script>

### Required libraries
---

* none

### API Description
---

* quicksort

```cpp
/*
  desc : quicksort algorithm
  parm :
  |- array_data : all data in array for sorting
  |- left : left boundary
  |- right : right boundary
  oupt : data array already sorted
  e.g. :
  int data[] = {1, -1, 2, 5, -3, 5, 7, 9, -10, 10};
  quicksort(data, 0, 10);
*/
void quicksort(int array_data[], int left, int right);
```
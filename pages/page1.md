---
title: Example page1
---

```sql aaa
select date, name, count from read_csv_auto('sources/test.csv', HEADER=TRUE)
```

<BarChart
  data={aaa}
  x=date
  y=count
  series=name
/>

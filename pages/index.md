---
title: Evidence Example
---

```sql build_time
select * from read_csv_auto('sources/build_time.csv', HEADER=TRUE)
```

Build At: <Value data={build_time} column=date /> <Value data={build_time} column=time /> <Value data={build_time} column=zone />

テキストメッセージ

test message

```sql aaa
select date, name, count from read_csv_auto('sources/test.csv', HEADER=TRUE)
```

<BarChart
  data={aaa}
  x=date
  y=count
  series=name
/>


```sql aaa2
select date as date_ddd, name, count as count_usd from read_csv_auto('sources/test.csv', HEADER=TRUE)
```

<BarChart
  data={aaa2}
  x=date_ddd
  y=count_usd
  series=name
/>

```sql bbb
select name, value/60 as value_num2 from read_csv_auto('sources/test2.csv', HEADER=TRUE)
```

<BarChart
  data={bbb}
  x=name
  y=value_num2
  swapXY=true
/>

```sql ccc
select * from read_csv_auto('sources/test3.csv', HEADER=TRUE)
where date > '2023-06-05'
```

```` markdown
```r
df |>
  summarise(across(bill_length_mm,                         # <1>
                   list(mean = \(x) mean(x, na.rm = TRUE), # <2>
                        sd   = \(x) sd(x, na.rm = TRUE))   # <2>
                   ),
            .by = species)                                 # <3>

```

1. 対象となる変数
2. 計算部分
3. グループ別に出すときに指定

````
# Dividends APIs

Requires authentication.

## Get Dividends

Returns all dividends.

```APIs
GET https://dev.zoomsymbols.com/api/dividends/getDividends
```


> Response

```json
{
    totalRecords: "282451",
    totalPages: 2825,
    pageSize: 100,
    pageNum: null,
    columns: [...],
    order: {
        column: "gross_amount",
        order: "desc"
    },
    result: [{
        symbol_id: "1361691",
        symbol_value: "RCC",
        symbol_name: "Small Cap Premium & Dividend Income Fund Inc.",
        corp_action_sub_type: "Includes extra, special, participating dividends, arrears, and liquidations",
        corp_action_type: "Dividend",
        corp_action_rate: "10.3793700000",
        ex_date: "2010-05-24T00:00:00.000Z",
        pay_date: "2010-05-24T00:00:00.000Z",
        record_date: "2010-05-24T00:00:00.000Z",
        announced_date: null,
        currency_name: "US Dollar",
        frequency_type: null,
        applied_flag: false,
        gross_amount: "10.3793700000",
        net_amount: null,
        chg_1d: "0.0300",
        return_1d: "0.2899",
        px_open: "10.35",
        px_high: "10.38",
        px_low: "10.35",
        px_close: "10.38",
        volume: "135330",
        totalRecords: "282451"
    }, ...]
}
```

## Get Dividends

Returns all dividends.

```APIs
GET https://dev.zoomsymbols.com/api/dividends/getDividendsSort
```

> Parameters

```
sortBy: sort_by (default 'gross_amount')
```

> Response

```json
{
    error: null,
    result: [{
            code: "highest_current_yield",
            name: "Highest Current Yield"
        },
        {
            code: "latest_ex_div_date",
            name: "Latest Ex-Div Date"
        },
        {
            code: "latest_pay_dated",
            name: "Latest Pay Date"
        }
    ]
}
```

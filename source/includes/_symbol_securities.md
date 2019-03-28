# Symbol Securities APIs

Requires authentication.

## Get Data

Returns all symbol securities data.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-securities/getData
```

> Response

```json
{
    totalRecords: "290",
    totalPages: 3,
    pageSize: 100,
    pageNum: null,
    columns: [...],
    order: {
        column: "return_1d",
        order: "desc"
    },
    result: [{
        px_date: "2019-03-27T00:00:00.000Z",
        symbol_id: "1468437",
        symbol_value: "NWHM",
        symbol: "NWHM",
        symbol_name: "The New Home Company Inc.",
        chg_1d: "0.4000",
        return_1d: "8.8889",
        px_open: "4.50",
        px_high: "4.92",
        px_low: "4.50",
        px_close: "4.90",
        chart_data: [{
                date: "2019-03-21",
                value: 4.62
            },
            {
                date: "2019-03-22",
                value: 4.52
            },
            {
                date: "2019-03-25",
                value: 4.48
            },
            {
                date: "2019-03-26",
                value: 4.5
            },
            {
                date: "2019-03-27",
                value: 4.9
            }
        ],
        trends_direction: "UP",
        trends_days: "2.00",
        totalRecords: "290"
    }, ...]
}
```

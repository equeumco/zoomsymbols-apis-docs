# Symbol Prices APIs

Requires authentication.

## Get Prices

Returns all prices for given symbol.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-prices/getPrices
```

> Response

```json
{
    totalRecords: "5954",
    totalPages: 60,
    pageSize: 100,
    pageNum: null,
    columns: [...],
    order: {
        column: "px_date",
        order: "desc"
    },
    result: [{
        px_date: "2019-03-27",
        symbol_id: "34379",
        symbol_value: "MSF",
        symbol: "MSF",
        symbol_name: "Microsoft Corporation",
        chg_1d: "-0.1300",
        return_1d: "-0.1251",
        px_open: "104.66",
        px_high: "105.21",
        px_low: "102.78",
        px_close: "103.82",
        volume: "3315",
        totalRecords: "5954"
    }, ...]
}
```

## Get Data

Returns all data for a given symbol.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-prices/getData
```

> Parameters

```
symbol: your_symbol
field: your_field (e.g 'px_close')
```

> Response

```json
{
    totalRecords: "8328",
    totalPages: 84,
    pageSize: 100,
    pageNum: null,
    columns: [...],
    order: {
        column: "px_date",
        order: "desc"
    },
    result: [{
        px_date: "2019-03-28",
        symbol_id: "68",
        symbol_value: "MSFT",
        symbol: "MSFT",
        symbol_name: "Microsoft Corporation",
        px_close: "117.16",
        totalRecords: "8328"
    }, ...]
}
```

## Get Charts

Returns all charts for a given symbol id.

```APIs
https://dev.zoomsymbols.com/api/symbol-prices/getCharts
```

> Parameters

```
symbolId: your_symbol
```

> Response

```json
{
    result: [{
        code: "symbol_name",
        title: "Name",
        data: [{
            date: "2003-04-25",
            value: 0.25
        }, ...]
    }]
}
```

# Corp Actions APIs

Requires authentication.

## Get Corp Action Types

Returns all corp actions types.

```APIs
GET https://dev.zoomsymbols.com/api/corp-actions/getCorpActionTypes
```

> Response

```json
{
    result: [{
            code: "dividend",
            name: "Dividend"
        },
        {
            code: "split",
            name: "Split"
        }
    ]
}
```

## Get Corp Action Exchanges

Returns all corp actions exchanges.

```APIs
GET https://dev.zoomsymbols.com/api/corp-actions/getCorpActionsExchanges
```

> Response

```json
{
    result: [{
        exchange_id: 2,
        exchange_code: "ASX",
        exchange_name: "Australian Securities Exchange"
    }, ...]
}
```
## Get Corp Action Data

Returns all corp actions data.

```APIs
GET https://dev.zoomsymbols.com/api/corp-actions/getCorpActionData
```

> Response

```json
{
    totalRecords: "4422",
    totalPages: 45,
    pageSize: 100,
    pageNum: null,
    columns: [{
            code: "symbol_value",
            name: "Symbol",
            enableSort: true,
            styles: {
                textAlign: "left"
            },
            width: 150,
            onPress: {
                navigateTo: {
                    screen: "Symbol",
                    params: {
                        symbolItem: {
                            symbol_id: "{symbol_id}",
                            symbol_value: "{symbol_value}",
                            symbol_name: "{symbol_name}"
                        }
                    }
                }
            }
        },
        {
            code: "corp_action_rate",
            name: "Rate",
            enableSort: true,
            styles: {
                textAlign: "right"
            },
            format: {
                type: "number",
                cellsFormat: "d",
                formatValue: "2",
                enableSort: true
            },
            width: 160
        }, ...
    ]
}
```

## Get Corp Action Data For Symbol

Returns all corp action data for a given symbol.

```APIs
GET https://dev.zoomsymbols.com/api/corp-actions/getCorpActionDataForSymbol
```

> Parameters

```
symbol/symbolId: your_symbol
```

> Response

```json
{
    totalRecords: "63",
    totalPages: 1,
    pageSize: 100,
    pageNum: null,
    columns: [...],
    order: {
        column: "a.announced_date",
        order: "desc"
    },
    result: [{
        symbol_id: "34379",
        symbol_value: "MSF",
        symbol: "MSF",
        symbol_name: "Microsoft Corporation",
        corp_action_type_name: "Dividend",
        corp_action_rate: "0.4600000000",
        ex_date: "2019-05-15T00:00:00.000Z",
        pay_date: "2019-06-13T00:00:00.000Z",
        record_date: "2019-05-16T00:00:00.000Z",
        totalRecords: "63"
    }, ...]
}
```

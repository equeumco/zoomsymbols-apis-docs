# Symbol Mover APIs

Requires authentication.

## Get Mover Groups

Returns all mover groups.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-mover/getMoverGroups
```


> Response

```json
{
    result: [{
        view_name: "Top",
        children: [{
                id: 9,
                view_code: "top_gainers",
                view_name: "Top Gainers"
            },
            {
                id: 10,
                view_code: "top_gainers_percentage",
                view_name: "Top Gainers %"
            },
            {
                id: 11,
                view_code: "top_losers",
                view_name: "Top Losers"
            },
            {
                id: 12,
                view_code: "top_losers_percentage",
                view_name: "Top Losers %"
            }
        ]
    }, ...]
}
```

## Get Mover Data

Returns all mover data.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-mover/getMoverData
```

> Response

```json
{
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
            code: "px_close",
            name: "Close Price",
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
            width: 150
        }, ...
    ]
}
```

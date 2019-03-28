# Symbol Peers APIs

Requires authentication.

## Get Peers

Returns all symbol peers.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-peers/getPeersTags
```

> Parameters

```
symbol/symbolId: your_symbol
```

> Response

```json
{
    result: {
        company_sector: "Information Technology",
        company_industry_group: "Software & Services",
        company_industry_category: "Software"
    }
}
```

## Get Peers

Returns all peers for a given tag name and tag value.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-peers/getPeers
```

> Parameters

```
tagName: tag_name
tagValue: tag_value
filter: (default 'by_exchange')
symbolId (given if "filter" does not equal 'by_global')
```

> Response

```json
{
    totalRecords: "x",
    totalPages: x,
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
        },
        {
            code: "chart_data",
            name: "Chart 5 days",
            enableSort: false,
            format: {
                type: "chart",
                formatValue: "0",
                enableSort: false
            },
            width: 150
        }, ...
    ],
    result: [...]
}
```

## Get Peers Drop Down

Returns all peers drop downs.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-peers/getPeersDropDown
```

> Response

```json
{
    result: {
        by_exchange: [{
                code: "by_exchange",
                name: "Exchange",
                group_code: "by_exchange",
                group_name: "By Exchange"
            },
            {
                code: "by_country",
                name: "Country",
                group_code: "by_exchange",
                group_name: "By Exchange"
            }
        ],
        by_region: [{
            code: "by_region_us",
            name: "US",
            group_code: "by_region",
            group_name: "By Region"
        }, ...]
    }
```

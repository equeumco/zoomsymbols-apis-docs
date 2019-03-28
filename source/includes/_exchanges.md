# Exchanges API

Requires authentication.

## Get Exchanges

Returns all exchanges.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchanges
```

> Response

```json
{
    totalRecords: "168",
    totalPages: 2,
    pageSize: 100,
    pageNum: null,
    message: "Please use /api/exchanges/getExchanges API",
    result: [{
        exchange_id: 409,
        exchange_code: "ADX",
        exchange_name: "Abu Dhabi Securities Exchange",
        country_id: 192,
        country_name: "United Arab Emirates",
        country_iso2: "AE",
        country_iso3: "ARE",
        region_id: 3,
        region: "Africa / Middle East",
        currency_id: 2,
        currency_name: "United Arab Emirates Dirham",
        iso_code: "AED",
        currency_code: "AED",
        exchange_parent_id: null,
        exchange_parent_code: null,
        exchange_parent_name: null,
        totalRecords: "168"
    }, ...]
}
```


## Get Exchanges Sources Drop Down

Returns all exchanges sources drop down.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesSourcesDropDown
```

> Parameters (OPTIONAL)

```
byExchange: true/false
byExchangeParent: true/false
```

> Response

```json
{
    result: {
        popular: [{
                code: "AU",
                name: "Australia"
            },
            {
                code: "FR",
                name: "France"
            },
            {
                code: "DE",
                name: "Germany"
            },
            {
                code: "JP",
                name: "Japan"
            },
            {
                code: "GB",
                name: "United Kingdom"
            },
            {
                code: "US",
                name: "United States"
            }
        ],
        ...]
      }
}
```


## Get Exchanges Overview

Returns all exchanges overviews.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesOverview
```

> Response

```json
{
    error: null,
    result: {
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
}
```

## Get Exchanges Shares Trading

Returns all exchanges shares trading.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesSharesTrading
```

> Response

```json
{
    result: {
        declines: "919",
        advanced: "1770",
        not_change: "79",
        columns: [{
                code: "advanced",
                name: "Advanced",
                enableSort: true,
                styles: {
                    textAlign: "right",
                    color: "#24e5a2"
                },
                format: {
                    type: "number",
                    formatValue: "2",
                    enableSort: true
                },
                width: 150,
                colorized: true
            },
            {
                code: "declines",
                name: "Declines",
                enableSort: true,
                styles: {
                    textAlign: "right",
                    color: "#ff7586"
                },
                format: {
                    type: "number",
                    formatValue: "2",
                    enableSort: true
                },
                width: 150,
                colorized: true
            },
            {
                code: "not_change",
                name: "Not Change",
                enableSort: true,
                styles: {
                    textAlign: "right",
                    color: "#ffffff"
                },
                format: {
                    type: "number",
                    formatValue: "2",
                    enableSort: true
                },
                width: 150,
                colorized: true
            }
        ]
    }
}
```

## Get Exchanges Most Active

Returns most active exchanges.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesMostActive
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
        },
        {
            code: "chg_1d",
            name: "Change $ 1 day",
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
    }]
}
```

## Get Exchanges Declines

Returns all declining exchanges

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesDeclines
```

> Response

```json
{
    ...
    result: [{
        px_date: "2019-03-27T00:00:00.000Z",
        symbol_id: "143728",
        symbol_value: "BRK.A",
        symbol: "BRK.A",
        symbol_name: "Berkshire Hathaway Inc.",
        chg_1d: "-1197.0100",
        return_1d: "-0.3977",
        px_open: "300851.00",
        px_high: "301480.74",
        px_low: "297900.00",
        px_close: "299764.00",
        chart_data: [{
                date: "2019-03-21",
                value: 307120
            },
            {
                date: "2019-03-22",
                value: 301225
            },
            {
                date: "2019-03-25",
                value: 299380
            },
            {
                date: "2019-03-26",
                value: 300961.01
            },
            {
                date: "2019-03-27",
                value: 299764
            }
        ],
        trends_direction: "DOWN",
        trends_days: "1.00"
    }, ...]
}
```

## Get Exchanges Advanced

Returns all advanced exchanges.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesAdvanced
```

> Response

```json
{
    ...
    result: [{
        px_date: "2019-03-28T00:00:00.000Z",
        symbol_id: "259712",
        symbol_value: "PVH",
        symbol: "PVH",
        symbol_name: "PVH Corp.",
        chg_1d: "19.4400",
        return_1d: "17.5309",
        px_open: "125.12",
        px_high: "132.36",
        px_low: "124.80",
        px_close: "130.33",
        chart_data: [{
                date: "2019-03-22",
                value: 107.21
            },
            {
                date: "2019-03-25",
                value: 109.19
            },
            {
                date: "2019-03-26",
                value: 110.1
            },
            {
                date: "2019-03-27",
                value: 110.89
            },
            {
                date: "2019-03-28",
                value: 130.33
            }
        ],
        trends_direction: "UP",
        trends_days: "4.00"
    }, ...]
}
```

## Get Security Types

Returns all security types.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getSecurityTypes
```

> Response

```json
{
    result: [{
            security_type_code: "equity",
            security_type_name: "Equity"
        },
        {
            security_type_code: "etf",
            security_type_name: "Exchange Traded Fund"
        },
        {
            security_type_code: "fund",
            security_type_name: "Fund"
        },
        {
            security_type_code: "commodity",
            security_type_name: "Commodity"
        },
        {
            security_type_code: "future",
            security_type_name: "Future"
        },
        {
            security_type_code: "bond",
            security_type_name: "Bond"
        },
        {
            security_type_code: "index",
            security_type_name: "Index"
        },
        {
            security_type_code: "indicator",
            security_type_name: "Indicator"
        }
    ]
}
```

## Get Exchanges Range DropDown

Returns exchanges range dropdown.

```APIs
GET https://dev.zoomsymbols.com/api/exchanges/getExchangesRangeDropDown
```

> Response

```json
{
    result: [{
            code: "latest",
            title: "Latest"
        },
        {
            code: "historical",
            title: "Historical",
            show_custom_range: true
        }
    ]
}
```

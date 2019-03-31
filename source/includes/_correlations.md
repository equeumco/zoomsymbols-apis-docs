# Correlations APIs

Requires authentication.

## List (Correlations)

Returns a list of all correlations depending on a given type.

```APIs
GET https://dev.zoomsymbols.com/api/user-correlations/list
```

> Parameters

```
type: your_type
```

> Response

```json
{
    result: [{
            id: 10209,
            name: "Goog vs FB 2001",
            title: "Goog vs FB 2001",
            user_id: "5cde2208-1078-11e8-ae1b-83714d76deca",
            display_name: "Akram 5 akamal",
            user_item_type_id: 3,
            user_item_type_code: "correlation",
            visibility_code: "O",
            visibility_name: "Open",
            list_order: null,
            create_date: "2019-02-25T09:28:02.059458",
            modify_date: "2019-02-25T09:28:02.059458",
            is_enable: true,
            is_deleted: false,
            visibility: "O",
            can_write: false,
            can_read: true,
            is_fav: false,
            item_data: {
                startDate: "2018-01-09T22:00:00+00:00",
                endDate: "2019-01-09T22:00:00+00:00",
                fromDate: 1515535200000,
                toDate: 1547071200000,
                days: 30,
                dataSources: [{
                        symbol_id: 68,
                        company_id: 21835,
                        symbol_value: "MSFT",
                        symbol: "MSFT",
                        symbol_name: "Microsoft Corporation",
                        exchange_id: 414,
                        exchange_code: "NasdaqGS",
                        exchange_name: "Nasdaq Global Select",
                        data_provider_id: 2,
                        exchange_country_name: "United States",
                        exchange_country_id: 194,
                        exchange_country_iso2: "US",
                        exchange_parent_code: "NASDAQ",
                        symbol_status_name: "Active",
                        security_type_code: "equity",
                        latest_px_date: "2019-03-29",
                        latest_px_open: 118.07,
                        latest_px_high: 118.32,
                        latest_px_low: 116.96,
                        latest_px_close: 117.94,
                        latest_volume: 25375220,
                        latest_chg_1d: 1.01,
                        latest_return_1d: 0.8638,
                        price_data_provider_id: 2,
                        latest_modify_date: "2019-03-30T02:01:24.524393+00:00",
                        exchange_currency_name: "US Dollar",
                        exchange_currency_code: "USD",
                        currency_name: "US Dollar",
                        currency_code: "USD",
                        row_id: 653,
                        is_active: true,
                        ciq_security_id: 2630412,
                        field_id: 8,
                        field_code: "px_close",
                        field_name: "Close Price",
                        datatype: "symbol"
                    },
                }]
        }, userCanEdit: false
    },
    ...]
}
```

## Get Correlations

Returns a list of all correlations depending on a given type.

```APIs
GET https://dev.zoomsymbols.com/api/user-correlations/getCorrelation
```

> Parameters

```
startDate: your_startdate (optional)
endDate: your_enddate (optional)
symbolId1: first_symbol
symbolId2: second_symbol
```

> Response

```json
{
    result: {
        settings: {
            symbolId1: "59",
            symbolId2: "154"
        },
        history: [{
            date: "2008-09-02",
            value: 0.19
        }, ...]
    }
}
```

## Get (Correlations)

Returns correlation item for given itemId.

```APIs
https://dev.zoomsymbols.com/api/user-correlations/get
```

> Parameters

```
itemId: your_item
```

> Response

```json
{
  result: [...]
}
```

# Symbol Quant APIs

Requires authentication.

## Get Symbol Quants

Returns symbol quants for a given symbol.

```APIs
GET https://dev.zoomsymbols.com/api/symbol-quant/getSymbolQuants
```

> Parameters

```
symbol/symbolId: your_symbol
```

> Response

```json
{
    result: [{
        symbol_id: "1338591",
        symbol_value: "SPY",
        symbol_name: "SPDR S&P 500 ETF Trust",
        px_date: "2012-10-10T00:00:00.000Z",
        quant_total_score: "71.10",
        quant_composite_quality: "94.80",
        quant_composite_global: "64.70",
        quant_composite_fundamental: "72.50",
        quant_composite_behavioral: "65.40",
        quant_composite_sentiment: "68.20",
        quant_composite_technical: "62.60"
    }, ...]
}
```

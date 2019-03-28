# Companies News APIs

Requires authentication.

## Get Company News

Returns all company news data.

```APIs
GET https://dev.zoomsymbols.com/api/companies-news/getCompanyNews
```

> Response

```json
{
    totalRecords: "1688263",
    totalPages: 16883,
    pageSize: 100,
    pageNum: null,
    result: [{
        id: "4957244",
        symbol_id: "271027",
        symbol_value: "BMCH",
        symbol: "BMCH",
        symbol_name: "BMC Stock Holdings, Inc.",
        title: "New Research Coverage Highlights Norwegian Cruise Line, Devon Energy, Tenneco, COUPA SOFTWARE, Galapagos NV, and BMC Stock — Consolidated Revenues, Company Growth, and Expectations for 2019",
        summary: "NEW YORK, March 28, 2019 -- In new independent research reports released early this morning, Fundamental Markets released its latest key findings for all current investors,.",
        publication_date: "2019-03-28T11:00:00.000Z",
        url: "https://finance.yahoo.com/news/research-coverage-highlights-norwegian-cruise-110000030.html?.tsrc=rss",
        totalRecords: "1688263"
    }, ...]
}
```

## Get News Favourite

Returns favorite news for currently authorized user.


```APIs
GET https://dev.zoomsymbols.com/api/companies-news/getNewsFavourite
```

> Response

```json
{
  result: [...]
}
```

## Set News Favorite

Adds given news to the favorite list

```APIs
POST https://dev.zoomsymbols.com/api/companies-news/setNewsFavourite
```

> Parameters

```json
{
  newsId: news_id
}
```

> Response

```json
{
    "result": "succes"
}
```

## Delete News Favorite

Deletes given news from the favorite list

```APIs
POST https://dev.zoomsymbols.com/api/companies-news/deleteNewsFavourite
```

> Parameters

```json
{
  newsId: news_id
}
```

> Response

```json
{
    "result": "succes"
}
```

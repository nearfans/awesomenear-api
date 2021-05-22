## Awesome NEAR API

The Awesome NEAR data can be accessed via our RESTful JSON API `https://awesomenear.com/api`.

| Endpoints                | Description |
| ------------------------ | ------------------------------ |
| /api                     | Get a list of all projects. |
| /api/{:slug}             | Get a given project detail (project slug required). |
| /api/categories          | Get a list of all categories. |
| /api/categories/{:slug}  | Get a list of projects under given category (category slug required). |

### Endpoint `/api`

Endpoint example: `https://awesomenear.com/api`

Response:

```
{
  "title": "Awesome NEAR",
  "count": "135",
  "data": [
    {
      "title": "NEAR Protocol",
      "slug": "near-protocol",
      "description": "The highly scalable, developer-friendly blockchain.",
      "link": "https://awesomenear.com/near-protocol/",
      "categories": [
        "Infrastructure"
      ]
    },
    ...
  ]
}
```

### Endpoint `/api/{:slug}`

Endpoint example: `https://awesomenear.com/api/`

Response:

```
{
    "name": "NEAR Protocol",
    "slug": "near-protocol",
    "description": "The highly scalable, developer-friendly blockchain.",
    "permalink": "https://awesomenear.com/near-protocol/",
    "logo": "https://awesomenear.com/img/logo/near-protocol.jpg",
    "categories": [
        "Infrastructure"
    ],
    "social": {
        "blog": "https://near.org/blog/",
        "discord": "https://discordapp.com/invite/gBtUFKR",
        "facebook": "https://www.facebook.com/nearprotocol",
        "github": "https://github.com/nearprotocol",
        "medium": "https://medium.com/nearprotocol",
        "telegram": "https://t.me/cryptonear",
        "twitter": "https://twitter.com/nearprotocol",
        "website": "https://near.org/"
    },
    "content": "NEAR is a decentralized application platform that is secure enough to manage high value assets like money or identity and performant enough to make them useful for everyday people, putting the power of the Open Web in their hands."
}
```

### Endpoint `/api/categories`

Endpoint example: `https://awesomenear.com/api/categories`

Response:

```
{
    "title": "Categories",
    "count": "27", // The number of all categories
    "data": [
        {
            "title": "DApps",
            "slug": "dapps",
            "count": 57, // The number of projects under the DApps category
            "link": "https://awesomenear.com/categories/dapps/"
        },
        ...
    ]
}
```

### Endpoint `/api/categories/{:slug}`

Endpoint example: `https://awesomenear.com/api/categories/dapps/`

Response:

```
{
    "title": "DApps",
    "count": "57", // The number of projects under the DApps category
    "data": [
        {
            "title": "Flux",
            "slug": "flux",
            "description": "The easiest protocol for developers launching open financial markets.",
            "link": "https://awesomenear.com/flux/",
            "categories": [
                "DApps",
                "DeFi",
                "Oracles",
                "AMM",
                "OWC"
            ],
        },
        ...
    ]
}
```

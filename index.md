---
title: API Reference

language_tabs:
- bash
- javascript

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.

<!-- END_INFO -->

#Authentication


APIs for managing users
<!-- START_a4196a8491fd316d7c1eef8cfa3d07c8 -->
## Get Token

Get Token on app launch

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/get-token" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"device_type":"harum","device_id":"saepe"}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/get-token"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "device_type": "harum",
    "device_id": "saepe"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "auth": {
            "token": "tjl7UQmIcyejr2-HI2j7hCY_2878KA7H",
            "type": "Bearer"
        }
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/get-token`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `device_type` | string |  required  | Device type (A/I).
        `device_id` | string |  required  | Device unique id.
    
<!-- END_a4196a8491fd316d7c1eef8cfa3d07c8 -->

<!-- START_8c0e48cd8efa861b308fc45872ff0837 -->
## Login

Login to application

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"social_id":"praesentium","social_type":18,"full_name":"error","device_type":"dolores","device_id":"reiciendis"}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "social_id": "praesentium",
    "social_type": 18,
    "full_name": "error",
    "device_type": "dolores",
    "device_id": "reiciendis"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "Success",
        "user": {
            "user_id": 12,
            "full_name": "John",
            "email": "test@gmail.com",
            "profile_image": "https:\/\/picsum.photos\/id\/842\/200\/300",
            "points": 100,
            "referral_code": "XRE1212",
            "is_social": 1,
            "is_merge": 1,
            "is_hd_media_enabled": 1,
            "is_night_mode_enabled": 1,
            "is_notification_enabled": 1,
            "is_read_offline_enabled": 1,
            "is_lock_screen_enabled": 1,
            "category_ids": "1,2,3"
        }
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/login`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `social_id` | string |  required  | Social id.
        `social_type` | integer |  required  | Facebook/Google.
        `full_name` | string |  required  | Full name.
        `device_type` | string |  required  | Device type (A/I).
        `device_id` | string |  required  | Device unique id.
    
<!-- END_8c0e48cd8efa861b308fc45872ff0837 -->

<!-- START_fb2ae43e2e99ff4e90f22ba03801a735 -->
## Logout

Logout from application

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "Logout successfully"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/logout`


<!-- END_fb2ae43e2e99ff4e90f22ba03801a735 -->

<!-- START_6279964f390370bc5e7967cf563fd9ae -->
## App installation

Manage app installation count

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app-installation" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"unique_device_id":"fuga"}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/app-installation"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "unique_device_id": "fuga"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/app-installation`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `unique_device_id` | string |  required  | Device unique id.
    
<!-- END_6279964f390370bc5e7967cf563fd9ae -->

#News


APIs for managing news
<!-- START_1ed41f9935afda261b40f3e4179acf9b -->
## News list

Get news list

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/news-list" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":15,"limit":15,"search_keyword":"ullam","category_ids":"doloremque","is_bookmarked":true,"news_id":15}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/news-list"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 15,
    "limit": 15,
    "search_keyword": "ullam",
    "category_ids": "doloremque",
    "is_bookmarked": true,
    "news_id": 15
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "error": [],
    "data": {
        "news_list": [
            {
                "news_id": 76903,
                "media_type": 1,
                "media": "https:\/\/www.nagpurtoday.in\/wp-content\/uploads\/2019\/07\/Vishal-Muttemwar.jpg",
                "title": "Muttemwar demands scrapping of Mahapariksha Portal’ for recruitment in Govt departments",
                "description": "Nagpur : Maharashtra Pradesh Congress Committee (MPCC) Secretary Vishal Muttemwar has demanded Chief Minister Uddhav Thackeray to scrap 'Mahapariksha Portal' ",
                "article_source_link": "https:\/\/www.nagpurtoday.in\/muttemwar-demands-scrapping-of-mahapariksha-portal-for-recruitment-in-govt-departments\/12041840",
                "publisher_name": "Nagpurtoday",
                "datetime": "1575470273",
                "is_ad": 0,
                "is_bookmarked": 0,
                "shorten_url": "",
                "resize_media": "",
                "title_font": "",
                "description_font": "",
                "title_font_size": 10,
                "description_font_size": 20,
                "source_url": "https:\/\/127.0.0.1:8001\/news\/NzY5MDN8fDlQeFI123"
            }
        ],
        "ad_config": {
            "side_menu_bottombar_adtype": 2,
            "interestial_is_google_ad": 1,
            "interestial_is_admin_ad": 1,
            "google_ad_frequency": 12,
            "admin_ad_frequency": 13,
            "interstial_ads": [
                {
                    "ad_id": 319,
                    "title": "tets",
                    "media_type": 1,
                    "ad_click_url": null,
                    "image_url": "https:\/\/picsum.photos\/id\/842\/200\/300",
                    "description": "fdsf",
                    "title_font": "sailec-thin;",
                    "description_font": "",
                    "title_font_size": 1,
                    "description_font_size": null
                }
            ],
            "side_menu_bottombar_ads": []
        },
        "notification_count": 2,
        "get_points": {
            "current_points": 407,
            "eligibility_points": 0,
            "redeemed_points_share": 0,
            "referal_code": "OZKCXFL1",
            "referral_points_share": 10,
            "is_personalised": 0
        },
        "is_last": 1,
        "message": "Success"
    },
    "success": 1
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/news-list`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit variable.
        `search_keyword` | string |  optional  | Search keyword.
        `category_ids` | string |  optional  | Comma separated ids(1,2,3).
        `is_bookmarked` | boolean |  optional  | (1/0).
        `news_id` | integer |  optional  | To Get single news.
    
<!-- END_1ed41f9935afda261b40f3e4179acf9b -->

<!-- START_42c79b31e3f219c0252f25c34cac2d1f -->
## Bookmark

Make news as bookmarked

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/makebookmark" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"news_id":13,"is_bookmarked":false}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/makebookmark"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "news_id": 13,
    "is_bookmarked": false
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/makebookmark`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `news_id` | integer |  required  | News Id.
        `is_bookmarked` | boolean |  required  | (1/0).
    
<!-- END_42c79b31e3f219c0252f25c34cac2d1f -->

<!-- START_5598d7e6bec47cbbba9cf7e5aa67b658 -->
## Short url

Generate news short url

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/create-short-url" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"news_id":9,"slashtag":"rerum"}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/create-short-url"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "news_id": 9,
    "slashtag": "rerum"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success",
        "url": "dais.world\/test"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/create-short-url`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `news_id` | integer |  required  | News Id.
        `slashtag` | string |  required  | Provide slash tag to append after shorturl.
    
<!-- END_5598d7e6bec47cbbba9cf7e5aa67b658 -->

<!-- START_fcdbfcb5ff7d0fd12fa5ebcaeec3c0c1 -->
## Search news

Get news data by keywords

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/search-list" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"search_keyword":"et","start":18,"limit":4}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/search-list"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "search_keyword": "et",
    "start": 18,
    "limit": 4
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "search_list": [
            {
                "news_id": 1,
                "category_id": 2,
                "category_name": "Lifestyle News",
                "description": "Do Conspiracy theorists have it right this time",
                "title": "Coronavirus - The Disease X  - Do Conspiracy theorists have it right this time?",
                "is_selected": 1
            },
            {
                "news_id": 80629,
                "category_id": 10,
                "category_name": "Trending",
                "description": "test  summarizarion",
                "title": "test for summarizarion",
                "is_selected": 1
            }
        ],
        "is_last": 1,
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/search-list`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `search_keyword` | string |  optional  | Search keyword.
        `start` | integer |  optional  | Start variable.
        `limit` | integer |  optional  | limit count.
    
<!-- END_fcdbfcb5ff7d0fd12fa5ebcaeec3c0c1 -->

<!-- START_c62630e3a17e8ff62dde27c27ddd68b4 -->
## Trending post

Add news count to manage news as trending

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/trending-post" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"news_id":17}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/trending-post"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "news_id": 17
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/trending-post`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `news_id` | integer |  required  | News Id.
    
<!-- END_c62630e3a17e8ff62dde27c27ddd68b4 -->

<!-- START_c3c71e2a21d885b3b9227bb655603470 -->
## Ad hits

Increase ad hits count

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/ad-hits-count" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"ad_id":17}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/ad-hits-count"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "ad_id": 17
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/ad-hits-count`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `ad_id` | integer |  required  | Ad Id.
    
<!-- END_c3c71e2a21d885b3b9227bb655603470 -->

#News categories


APIs for managing news caterories
<!-- START_4ffcea0708c719181fab25e9d966c77b -->
## Get new categories

Get all news categories

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/get-category-list" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":8,"limit":19}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/get-category-list"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 8,
    "limit": 19
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "category_list": [
            {
                "category_id": 1,
                "category_name": "Lifestyle News",
                "is_selected": 1
            },
            {
                "category_id": 2,
                "category_name": "Sports",
                "is_selected": 1
            }
        ],
        "is_last": 1,
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/get-category-list`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit count.
    
<!-- END_4ffcea0708c719181fab25e9d966c77b -->

<!-- START_1f75ce1380cdfef6a5852ec30753a02d -->
## Select categories

Get news categories by user

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/select-category" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"category_ids":"tempora"}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/select-category"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "category_ids": "tempora"
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/select-category`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `category_ids` | string |  required  | Comma separated ids(1,2,3).
    
<!-- END_1f75ce1380cdfef6a5852ec30753a02d -->

#Notifications


APIs for managing notifications
<!-- START_2aac74a55a8cbf02c71f91b92b1d9256 -->
## Notification list

Get user notification list

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/get-notification" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":7,"limit":2}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/get-notification"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 7,
    "limit": 2
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "notifications": [
            {
                "notification_id": 1,
                "notification_type": "voucher_redeem",
                "title": "Notification 1",
                "description": "Roger Federar's tears For former coach: Never Broke down like this",
                "image": "https:\/\/picsu m.photos\/200\/300",
                "is_read": 0,
                "datetime": 112121212,
                "redirection_id": 3
            }
        ],
        "is_last": 1,
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/get-notification`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit count.
    
<!-- END_2aac74a55a8cbf02c71f91b92b1d9256 -->

<!-- START_4640a758c84ac6ba83aebf4b710549f4 -->
## Clear notifications

Clear user notifications list

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/clear-notification" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/clear-notification"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/clear-notification`


<!-- END_4640a758c84ac6ba83aebf4b710549f4 -->

<!-- START_d1d934a8d643e0064dd378af7b30577e -->
## Read notifications

Mark notification as read

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/read-notification" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"notification_id":8}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/read-notification"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "notification_id": 8
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/read-notification`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `notification_id` | integer |  required  | Notification id.
    
<!-- END_d1d934a8d643e0064dd378af7b30577e -->

#Rewards


APIs for managing rewards
<!-- START_1804db10d49b2fd52cd324899a034ec7 -->
## Reward claim

Get Reward claim

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/reward-claim" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":7,"limit":14}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/reward-claim"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 7,
    "limit": 14
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "total_points": 1000,
        "level": 1,
        "level_name": "Gold",
        "is_last": 1,
        "voucher_list": [
            {
                "voucher_id": 1,
                "voucher_image": "https:\/\/picsum.photos\/200\/300",
                "voucher_name": "GOFREE",
                "currency_symbol": "₹",
                "discount_amount": 10,
                "points": 50
            }
        ],
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/reward-claim`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit count.
    
<!-- END_1804db10d49b2fd52cd324899a034ec7 -->

<!-- START_9b0786c057cbf9bc4cd84cbd61dc0c45 -->
## Transaction history

Get user transaction history

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/transaction-history" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":14,"limit":9}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/transaction-history"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 14,
    "limit": 9
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "total_points": 1000,
        "level": 1,
        "level_name": "Gold",
        "is_last": 1,
        "transaction_history": [
            {
                "transaction_id": 1,
                "datetime": 12345678,
                "description": "John generated short url",
                "earned_points": 10
            }
        ],
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/transaction-history`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit count.
    
<!-- END_9b0786c057cbf9bc4cd84cbd61dc0c45 -->

<!-- START_640e59ab19742c12967d271cbb37a6db -->
## URLInsight

Get URLInsight with view count

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/url-insight" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"start":8,"limit":19}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/url-insight"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "start": 8,
    "limit": 19
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "total_points": 1000,
        "level": 1,
        "level_name": "Gold",
        "is_last": 1,
        "url_insights": [
            {
                "id": 1,
                "datetime": 12345678,
                "insight_url": "https:\/\/cutt.ly\/test",
                "clicks": 5,
                "views": 5
            }
        ],
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/url-insight`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `start` | integer |  required  | Start variable.
        `limit` | integer |  required  | limit count.
    
<!-- END_640e59ab19742c12967d271cbb37a6db -->

<!-- START_313a61b7fc13ced4b0ec8d9e1b48a111 -->
## Redeem voucher

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/redeem-voucher" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"voucher_id":13,"voucher_type":11}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/redeem-voucher"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "voucher_id": 13,
    "voucher_type": 11
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "code": "XRE1212"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/redeem-voucher`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `voucher_id` | integer |  required  | Voucher id.
        `voucher_type` | integer |  required  | 1:redeem, 2:earn.
    
<!-- END_313a61b7fc13ced4b0ec8d9e1b48a111 -->

#Settings


APIs for managing settings
<!-- START_06c29ffc3fe4dd9c060b6bb7e75224c9 -->
## Update settings

Update user application settings

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/update-settings" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"is_hd_media":false,"is_night_mode":false,"is_notification":false,"is_read_offline":false,"is_lock_screen":false}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/update-settings"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "is_hd_media": false,
    "is_night_mode": false,
    "is_notification": false,
    "is_read_offline": false,
    "is_lock_screen": false
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "Settings have been updated successfully"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/update-settings`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `is_hd_media` | boolean |  required  | HD media enabled.
        `is_night_mode` | boolean |  required  | Night mode enabled.
        `is_notification` | boolean |  required  | Notifications enabled.
        `is_read_offline` | boolean |  required  | Read offline enabled.
        `is_lock_screen` | boolean |  required  | Lock screen enabled.
    
<!-- END_06c29ffc3fe4dd9c060b6bb7e75224c9 -->

<!-- START_3f501cf4bba08a8acae3ef8a0f195e60 -->
## CMS

Get all cms pages

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/cms" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/cms"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "terms_and_conditions": "https:\/\/dais.world\/tc",
        "privacy_policy": "https:\/\/dais.world\/privacy",
        "twitter_url": "https:\/\/twitter.com\/dais",
        "facebook_url": "https:\/\/facebook.com\/dais",
        "linkedin_url": "https:\/\/linkedin.com\/dais",
        "url": "https:\/\/dais.world",
        "sitemap_link": "https:\/\/dais.world\/sitemap.xml",
        "copyright_year": "Copyright @Dais 2020"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/cms`


<!-- END_3f501cf4bba08a8acae3ef8a0f195e60 -->

<!-- START_f22af92f6f1ad0b3d8563eeee5a612e9 -->
## User points

Get user points

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/user-points" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/user-points"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "notification_count": 10,
        "current_points": 400
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/user-points`


<!-- END_f22af92f6f1ad0b3d8563eeee5a612e9 -->

<!-- START_615df04e637bb8ef13881f613ca7a8fb -->
## Update points

Update user points on app share/first login

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/update-points" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"points_type":15}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/update-points"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "points_type": 15
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/update-points`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `points_type` | integer |  required  | 1/2:  App share,3: 5 sec use, 4: First time login.
    
<!-- END_615df04e637bb8ef13881f613ca7a8fb -->

<!-- START_79061428d8bfca34e8fd3cecfe18e002 -->
## App Usages

Update user points on app usages login

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/app-usage" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}" \
    -d '{"is_counter_enable":true}'

```

```javascript
const url = new URL(
    "http://localhost/api/v1/app-usage"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

let body = {
    "is_counter_enable": true
}

fetch(url, {
    method: "POST",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "message": "success"
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/app-usage`

#### Body Parameters
Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    `is_counter_enable` | boolean |  required  | 1/0.
    
<!-- END_79061428d8bfca34e8fd3cecfe18e002 -->

<!-- START_9a955ed0f1eaa4dd4d3e07f65e62c468 -->
## FAQ

Get all FAQs

> Example request:

```bash
curl -X POST \
    "http://localhost/api/v1/faq" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json" \
    -H "Authorization: Bearer {token}"
```

```javascript
const url = new URL(
    "http://localhost/api/v1/faq"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "Authorization": "Bearer {token}",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```


> Example response (200):

```json
{
    "success": 1,
    "error": [],
    "data": {
        "faqs_list": [
            {
                "id": 1,
                "que": "question1",
                "ans": "answer1"
            },
            {
                "id": 2,
                "que": "question2",
                "ans": "answer2"
            }
        ]
    }
}
```
> Example response (404):

```json
{
    "error": [
        "Bad Request"
    ],
    "data": [],
    "success": 0
}
```

### HTTP Request
`POST api/v1/faq`


<!-- END_9a955ed0f1eaa4dd4d3e07f65e62c468 -->



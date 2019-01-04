# MojiLaLa Partnership REST API Documentation

We handle millions of requests a day. 

40,000+ original stickers by 500+ artists all over the world.



The MojiLaLa API that provide animated and static stickers in the responses. The available endpoints are as follows:

+ [Sticker Search](#sticker-search-endpoint)
+ [Sticker Trending](#sticker-trending-endpoint)
+ [Sticker Roulette (Random)](#sticker-roulette-random-endpoint)

### STICKER API PUBLIC KEY : dc6zaTOxFJmzC 

Note: the public key is subject to watermark constraints. We do not encourage live production deployments to use the public key.

### STICKER Search Endpoint 

Search all MojiLaLa Stickers for a word or phrase. Punctuation will be stripped and ignored. Use a plus or url encode for phrases. Example paul+rudd, happy+easter or american+psycho.. Example [cat](https://api.mojilala.com/v1/stickers/search?q=cat&api_key=dc6zaTOxFJmzC)

    https://api.mojilala.com/v1/stickers/search?q=cat&api_key=dc6zaTOxFJmzC 
    
###### Path

    /v1/stickers/search

###### Parameters

+ q - search query term or phrase
+ limit - (optional) number of results to return, maximum 100. Default 25
+ offset - (optional) results offset, defaults to 0
+ rating - limit results to those rated (y,g, pg, pg-13 or r).
+ lang - (optional) specify default country for regional content; format is 2-letter ISO 639-1 country code. See list of supported langauges [here](#language-support)
+ fmt - (optional) return results in html or json format (useful for viewing responses as IMAGESs to debug/test)

### Sample Response: Search

* if sticker is not animated
    
```json
{
  "data": [
    {
      "id": "U3RpY2tlci05NjM=",
      "is_animated": false,
      "url": "https://mojilala.com/stickers-emojis/stickers/U3RpY2tlci05NjM=",
      "rating": "g",
      "images": {
        "fixed_height": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHl6imPtJiw5JK2d1H8X8y1OlI7ES88kUb8tqxoEgTdE7l6NTdorCEBr5hGY5pkhvh.png",
          "width": 105,
          "height": 200,
          "size": 28819,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHl6imPtJiw5JK2d1H8X8y1OlI7ES88kUb8tqxoEgTdE4wk6pOszlaXhLc7hofM7f7.webp",
          "webp_size": 11230
        },
        "fixed_height_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHl6imPtJiw5JK2d1H8X8y1OlI7ES88kUb8tqxoEgTdE7l6NTdorCEBr5hGY5pkhvh.png",
          "width": 105,
          "height": 200,
          "size": 28819
        },
        "fixed_height_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+RaiEzRmYcHFZb2Jxvh0O7WmuQRhk1j/EB/Eu3u2IddSIwu6xjuT/FsWBCuCKsiZXDWd+RwpB02hvHnQ+7VtmTKsAMgQYA2xbycU5M/mbTlkg==.png",
          "width": 105,
          "height": 200,
          "size": 7782,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+RaiEzRmYcHFZb2Jxvh0O7WmuQRhk1j/EB/Eu3u2IddSIwu6xjuT/FsWBCuCKsiZXDWd+RwpB02hvHnQ+7VtmTKC/j4shc9LZcW8ydjhuLvyg==.webp",
          "webp_size": 7202
        },
        "fixed_height_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxG6E65lsR6pfT0+Pkf8VCoMtGFTrVPERleivj81eI2Uzp03KNXcOCdwhiFldGELLO.png",
          "width": 168,
          "height": 320,
          "size": 61308,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxG6E65lsR6pfT0+Pkf8VCoMtGFTrVPERleivj81eI2Uy7XAsbA/v7wqGWhrR9xTPv.webp",
          "webp_size": 17434
        },
        "fixed_height_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxG6E65lsR6pfT0+Pkf8VCoMtGFTrVPERleivj81eI2Uzp03KNXcOCdwhiFldGELLO.png",
          "width": 168,
          "height": 320,
          "size": 61308
        },
        "fixed_height_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPuW2taGunGdgT31tffeBrV6FcU7TN+9mPhmHL3lsql5ANLGAcmdVdU5LeWyXwDR5I/sXKY+0SzRC6eUKikVpl/eRgejGSnSbfhyZMMxrra8IQ==.png",
          "width": 168,
          "height": 320,
          "size": 14083,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPuW2taGunGdgT31tffeBrV6FcU7TN+9mPhmHL3lsql5ANLGAcmdVdU5LeWyXwDR5I/sXKY+0SzRC6eUKikVpl/e/HbdIs0gYXMpjcAW8XN41w==.webp",
          "webp_size": 12674
        },
        "fixed_width": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qqu1figY2cJSvpqgb5FqAyZoBRf4JxH8Bi7UoNJDTTWn8yhsrOjo0Gn+hD3gx4ciz.png",
          "width": 200,
          "height": 381,
          "size": 79761,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qqu1figY2cJSvpqgb5FqAyZoBRf4JxH8Bi7UoNJDTTWkVaDFGX+YYqY4MPOIcPxBd.webp",
          "webp_size": 20532
        },
        "fixed_width_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qqu1figY2cJSvpqgb5FqAyZoBRf4JxH8Bi7UoNJDTTWn8yhsrOjo0Gn+hD3gx4ciz.png",
          "width": 200,
          "height": 381,
          "size": 79761
        },
        "fixed_width_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRbAieyt2gaeQZV+BtprejzCqVc4vggX2Y0ydezFXNSOw5v0Ug9WnHEhw2YmQ6Agq/drDcTOm9R3qZl46nTV8C0KkzxXwh+/Dchgax4vZW3WVA==.png",
          "width": 200,
          "height": 381,
          "size": 18439,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRbAieyt2gaeQZV+BtprejzCqVc4vggX2Y0ydezFXNSOw5v0Ug9WnHEhw2YmQ6Agq/drDcTOm9R3qZl46nTV8C0KcEN5bSoLVyhR2fZG84pajw==.webp",
          "webp_size": 16578
        },
        "fixed_width_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZClaQbbWEIbIaWvIrRgX+KrcHmzC4yKvLOKH/fTTUMr6xK9vq2N3xc95gaUXz9+J3lk.png",
          "width": 320,
          "height": 610,
          "size": 162231,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZClaQbbWEIbIaWvIrRgX+KrcHmzC4yKvLOKH/fTTUMr6xL9/PrGxjPOe2DJW9iv/fBp.webp",
          "webp_size": 30584
        },
        "fixed_width_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZClaQbbWEIbIaWvIrRgX+KrcHmzC4yKvLOKH/fTTUMr6xK9vq2N3xc95gaUXz9+J3lk.png",
          "width": 320,
          "height": 610,
          "size": 162231
        },
        "fixed_width_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFzkASGBnQRFtf0AaxcOkX2PCMzMvYDxZP7YHK9/mfgL8m+INy3fX9mOYhyzMKmDmbmtsAoZ010KkmcLSVM1g0PCeimwyDE1IxD9W5riNPvwqw==.png",
          "width": 320,
          "height": 610,
          "size": 37007,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFzkASGBnQRFtf0AaxcOkX2PCMzMvYDxZP7YHK9/mfgL8m+INy3fX9mOYhyzMKmDmbmtsAoZ010KkmcLSVM1g0PCZ7U28FsqiTXPKs5dAWrzLQ==.webp",
          "webp_size": 33128
        },
        "fixed_height_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3QAa7JZnj2c+JqKbvLSMKdR8zlp5N0gYyDxThNG3SL+tqayj/4dlTOQvvW8z82E2Y.png",
          "width": 52,
          "height": 100,
          "size": 12153,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3QAa7JZnj2c+JqKbvLSMKdR8zlp5N0gYyDxThNG3SL+u4QLMEq0vu3CQYz+utkAED.webp",
          "webp_size": 6520
        },
        "fixed_height_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3QAa7JZnj2c+JqKbvLSMKdR8zlp5N0gYyDxThNG3SL+tqayj/4dlTOQvvW8z82E2Y.png",
          "width": 52,
          "height": 100,
          "size": 12153
        },
        "fixed_width_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZQR9Oww2SdOo58U0Lz2oTOa9vS8t9jo6IIVvxLDQX7H9uKYJGKpJU2Up4LnYF8twP.png",
          "width": 100,
          "height": 191,
          "size": 27090,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZQR9Oww2SdOo58U0Lz2oTOa9vS8t9jo6IIVvxLDQX7H8Uv7y+xo+MApL1bUGV4hRe.webp",
          "webp_size": 10806
        },
        "fixed_width_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZQR9Oww2SdOo58U0Lz2oTOa9vS8t9jo6IIVvxLDQX7H9uKYJGKpJU2Up4LnYF8twP.png",
          "width": 100,
          "height": 191,
          "size": 27090
        }
      }
    },
    
    ... more items
  ],
  "meta": {
    "status": 200,
    "msg": "OK"
  },
  "pagination": {
    "total_count": 142,
    "count": 1,
    "offset": 0
  }
}

```

* if sticker is animated

```json
{
  "data": [
    {
      "id": "U3RpY2tlci0zMDg4MQ==",
      "is_animated": true,
      "url": "https://mojilala.com/stickers-emojis/stickers/U3RpY2tlci0zMDg4MQ==",
      "rating": "g",
      "images": {
        "fixed_height": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeLa1AEpmD1zEzPgm/HJgGgHMKGzJTCYhGYP4GAZdLITNN+AD9ru58J3gkXJq6o/6lW0O0JlQp7uPh8hOwblxT3XMEsAHMAa3Gq7UwodYB9/w==.gif",
          "width": 200,
          "height": 200,
          "size": 935705,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRNyiYdXJYJMpKN1aOTluoP6HGxFANgcR8bd9OsZuCqTM=.webp",
          "webp_size": 1124,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeLa1AEpmD1zEzPgm/HJgGgHMKGzJTCYhGYP4GAZdLITNN+AD9ru58J3gkXJq6o/6lW0O0JlQp7uPh8hOwblxT3Dpr4HjGVbSJemWvwSC6Pyg==.mp4",
          "mp4_size": 347033,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONfZ+hrJrQ6jC7+BwNShdhxyV+K0bIXtiqbwStR+8crI0oVAUWTaC1kIV7SjLUyyH4nz1ic3iSZ9hiA/u6zkykmq.png",
          "apng_size": 935705
        },
        "fixed_height_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYmDyYhdoHLQzdr889aSJblSTFFkqlz6BNrukI/pistZgyMHTUpx+9G/IBVmWdiXPozdZLxqpb6oqu8oy2TvfAj.png",
          "width": 200,
          "height": 200,
          "size": 1791
        },
        "fixed_height_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeLa1AEpmD1zEzPgm/HJgGghiTI0Uy8IcQpHmDATXlYF6ayceiByd/kY4y57PJVkuaz/uagThrBmUmcjCEaXXBIclRcoWqW+WAAULOvGB0q0MRkF//Hmxd8mCEzywvY2dg=.gif",
          "width": 200,
          "height": 200,
          "size": 71404,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRnEp3FCJ9gC3KKOxEzRLZBjyrCtuuBSR/8ITlmUbavlo=.webp",
          "webp_size": 420,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeLa1AEpmD1zEzPgm/HJgGghiTI0Uy8IcQpHmDATXlYF6ayceiByd/kY4y57PJVkuaz/uagThrBmUmcjCEaXXBIclRcoWqW+WAAULOvGB0q0EKGF5qAi3+gnLkjQMF7TMw=.mp4",
          "mp4_size": 11393,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeBFerKwDxFXEMSdOfj1Ff2byYGGQgMcLM7aytxcGn8FYaaoK9oN+j8OYPLZZe/i3UH9cMFFYMarkO1OxgCkS6/chjGas0tBWRYOJFzk+lU7zTkbDnpPE3P9N86TNflg6I=.png",
          "apng_size": 71404
        },
        "fixed_height_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9tZ/IErCtkWjFRwsJ5tRFniECvqImtfL/QxrTq+8WjkPmbgt+dOlkdJOIRv1l6Nnzi0TLPwTXLJim22nxojf9W+HNf6gTXGlzb0y5a4B10Dkg==.gif",
          "width": 320,
          "height": 320,
          "size": 1837430,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRFqpQwM8nTjMaAuR5AFskNOD99qmulU1gAX4e7tRcDHo=.webp",
          "webp_size": 1920,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9tZ/IErCtkWjFRwsJ5tRFniECvqImtfL/QxrTq+8WjkPmbgt+dOlkdJOIRv1l6Nnzi0TLPwTXLJim22nxojf9W+nefQTTbZO2KVkZiXTacmZQ==.mp4",
          "mp4_size": 736205,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9ssbylkZSphY+EIRwxu7r2zWvn3LqK9lLlo+K/0FSSdFh/uaIy0lkxYpws5gIuIjih+Cn3SA03u/DQKbbSKGFqd.png",
          "apng_size": 1837430
        },
        "fixed_height_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOudGYN1Z0KL+9dlziUdeGbywiN19QIdAef8o2+9TBZn8XSrwtQKeObgoMSAdu6dlHlQ1NBrgP3S6Ad10Ll4f59yT.png",
          "width": 320,
          "height": 320,
          "size": 3430
        },
        "fixed_height_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9tZ/IErCtkWjFRwsJ5tRFni9GBH9tOPqRqqH46a56YT6QxmPTjd3xPNLCNlbQaSBpcSruUSMfayvPtH0vmq3rlrbugO3Y1ARuiTxG1rgBILkRyFOLzbO62LVaLzLT0CdCU=.gif",
          "width": 320,
          "height": 320,
          "size": 139455,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRFqpQwM8nTjMaAuR5AFskNHwNtEcE/I/fD/y5klXnbvqKRZgrZ/X2KFIOQqtAtzeg.webp",
          "webp_size": 756,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9tZ/IErCtkWjFRwsJ5tRFni9GBH9tOPqRqqH46a56YT6QxmPTjd3xPNLCNlbQaSBpcSruUSMfayvPtH0vmq3rlrbugO3Y1ARuiTxG1rgBILkdn37NrJIAh1207VWLs2JD8=.mp4",
          "mp4_size": 20691,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9sy6A/1CEV4wMG6Y9Q+EIoXLaWg3JVPVpN514GzToYj4XerrR0oWVibOU7Y5yhdN4dSztHMnHUJUbmagMYPITaDQYK3A0X/BGzND1ldSz8BAdCg0zZ+nuBooytQzhhDvqA=.png",
          "apng_size": 139455
        },
        "fixed_width": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVAO95N2a7Nn+VfVoGr8EOvdRDtvgxRlX+WKOsnJzWT5UhkLnHze0WBE6+tItmTPOmc3HKamRX1JSUDbd0t+SyEqkfa3t7emR2u2xCRKiQGOXg==.gif",
          "width": 200,
          "height": 200,
          "size": 935705,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRvmNz2gygWFal1nfbGY+AlNDOEtVOK0uLPajsPorDh+Q=.webp",
          "webp_size": 1124,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVAO95N2a7Nn+VfVoGr8EOvdRDtvgxRlX+WKOsnJzWT5UhkLnHze0WBE6+tItmTPOmc3HKamRX1JSUDbd0t+SyEqctFhvFzr3XKG9k6YwDpBoA==.mp4",
          "mp4_size": 347033,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVA56BogN9O8x+N7V1le+9LI8171ZxXE5U5h7eeq68pEIHpN21aqBKjuZciLkPKH8qSED4aOUOOxanvoHdzZESD4.png",
          "apng_size": 935705
        },
        "fixed_width_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngAZpVffGH4aQZzpYfBsVErI4CvEz3q97RmiOeLc7JGRZOK085gAlleFR/LI3FFMDjmshbKQaaYPCkYAMrcK4vvw.png",
          "width": 200,
          "height": 200,
          "size": 1791
        },
        "fixed_width_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVAO95N2a7Nn+VfVoGr8EOvdaa5OJqM48Egqi0W0GSbu2tZPegwRTFehyB+yJcytxngZZVuqWQDm1RA8Fz+wU4lorytW4CJ3SGiqynn132VZ35NWv83eVGb6MKxttx47WXs=.gif",
          "width": 200,
          "height": 200,
          "size": 71404,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GR1OeyNC1hgDnA+5HqqyqtKsoPShFICisD7Sc8pxt0rwo=.webp",
          "webp_size": 420,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVAO95N2a7Nn+VfVoGr8EOvdaa5OJqM48Egqi0W0GSbu2tZPegwRTFehyB+yJcytxngZZVuqWQDm1RA8Fz+wU4lorytW4CJ3SGiqynn132VZ3ySHnmoXzuUa9t08lTtK7Mw=.mp4",
          "mp4_size": 11393,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVClsADZYSMVzXN47XwnquW/OehkVWQ3ax8Ur1/NrJTd2Kd1/mRwoiMCiAbu4I9i2W11aTTYLW0Kjss2Tdtvq06FZHOrKkG6pXFAm250XJ8QHjV/m2kDrY28aQ0/F6J6bHk=.png",
          "apng_size": 71404
        },
        "fixed_width_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxfUZ29CKjGsePpiSMLOmPyFDgy7DDDUoURWn2AmTfcLDyLH/Vbjyf1bBzCkFAT7VvSqHqgOddk4xT8AgI5KQibU+eq6jlNYBuS+9a2DHIql1A==.gif",
          "width": 320,
          "height": 320,
          "size": 1837430,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRsiJSxOwoKkKUUkasb1qI5a6qtjU5NIVryDaeiA3HorU=.webp",
          "webp_size": 1920,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxfUZ29CKjGsePpiSMLOmPyFDgy7DDDUoURWn2AmTfcLDyLH/Vbjyf1bBzCkFAT7VvSqHqgOddk4xT8AgI5KQibUg0l3dtvMoCHpBRaAk2dt8Q==.mp4",
          "mp4_size": 736205,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxeJtamMNLDGaijJJjAUbcsJPnQbpY89WXSlfKmmktK8JTC8q8umjceiLJeScM9Gq9o96G4Npcm9Nop+5Y+PP32B.png",
          "apng_size": 1837430
        },
        "fixed_width_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuH+3x0U4sYxfYIH5wxGMm7ggMvFf8gZ5mgsWnnb/8oHBcc0+63qffLLOmlRe7Lap0BsPFC5QiO+FIODD7UUQCvj.png",
          "width": 320,
          "height": 320,
          "size": 3430
        },
        "fixed_width_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxfUZ29CKjGsePpiSMLOmPyFldW4L3gT8yVIsQFVOLMcEPUI3UNNYDKmtlC6AFAm5Nnafehy2bFDrIqEWEvdfpcWEkNfkUX3GtkgywOeLJJ3imoM/CrxXAzk4BUwqiJ1uAw=.gif",
          "width": 320,
          "height": 320,
          "size": 139455,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRsiJSxOwoKkKUUkasb1qI5QB/JVAFXb+5xLwr8YkwNCKRukkKGVVMieLIxEZXwYJF.webp",
          "webp_size": 756,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxfUZ29CKjGsePpiSMLOmPyFldW4L3gT8yVIsQFVOLMcEPUI3UNNYDKmtlC6AFAm5Nnafehy2bFDrIqEWEvdfpcWEkNfkUX3GtkgywOeLJJ3irrNCQEDUoYD6O/SGmXVmK4=.mp4",
          "mp4_size": 20691,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxdJZJ2tMoGSXH5KcYXQK9f4bEWzx3aHD4v1ioX2L6hyBsIjnz9AEeTEKYXZdIkAfEuRSVd2Oxde/Bk/GsnbmiLvqWtDhW289YszsvWfaqVal8viiiu2klHlgclDN6zcHdU=.png",
          "apng_size": 139455
        },
        "fixed_height_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOT48VSmBWymKmKTfPviwtlHhpIhpFmme+m3apveYfEzzX7VUC36v3D5PCHXHE155H2bHpBegohWaOf5/Glaf52wxBKSxn/14DTYF+XStHfzv70x5V/JLjkm5cpizEEsv2lx5SDKrUhJnuPRxg1U/XydJAISKWQAKEgtxzxiUnM1VuXj9PMWCXKkOhN30Zop5Q==.gif",
          "width": 100,
          "height": 100,
          "size": 330425,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRfaVy7pE5FRrQ/av0/8qHpiL/nb20O8im23xpLgn9ZgY=.webp",
          "webp_size": 524,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOT48VSmBWymKmKTfPviwtlHhpIhpFmme+m3apveYfEzzX7VUC36v3D5PCHXHE155H2bHpBegohWaOf5/Glaf52wxBKSxn/14DTYF+XStHfzv70x5V/JLjkm5cpizEEsv2lx5SDKrUhJnuPRxg1U/XydJAISKWQAKEgtxzxiUnM1VsjpxWCjrN/bVX/AyQM80A==.mp4",
          "mp4_size": 111927,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOT48VSmBWymKmKTfPviwtlHhpIhpFmme+m3apveYfEzzX7VUC36v3D5PCHXHE155H2bHpBegohWaOf5/Glaf53thI9nOd/PI9N3P9oqRs56Rn/7u1XY+wMqoPtr6JAXQ5eLF1RVJRrtU4W3ZxF5eI2cJMgCzfRlOBiUP8rQIjgH.png",
          "apng_size": 330425
        },
        "fixed_height_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YJI9FDU38gx1cczoEc9+3zEciltwmmXXrJxyZDlgpSgerYVIkPx7C9HQlI90tv7WHmakL/UPv1enC/OsWirP1lu3xG7WuQhMFw1kOpaJDcvowrnb9V+mVcuQGYkO8yz72wvP1axwbOXLOjYf/q8C68iUb5Dlb3giKllEUcCrYEVR.png",
          "width": 100,
          "height": 100,
          "size": 913
        },
        "fixed_width_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YG9GUhudWHtZpAokKzEQ6tG1HsNz7CoJWFVAxhnz8YRvQgI9s9GKOhQwGBrbBDWrTj/qhZjGn7F1b80ygbuewcrVgdRGiw7LI/0w/MwP/2aYK+FZfmuRpvhMmTfqEuSxJYUp/hbWo8e0MgI9yrb1SS2OojdD1ltrkVg0Uv4zvC+0pdjT+/TwrlnGHT0tj6LZIw==.gif",
          "width": 100,
          "height": 100,
          "size": 330425,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgjixRho6YAZqsSW0j4o4MZZqN2VffsZyB+IPPjyTN9xyQnDqRtmOYRgTllZa9r+GRVFi7UqwKe1SQxv1LV/6hyAMAu1FALgQtZ+COT6huN0g=.webp",
          "webp_size": 524,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YG9GUhudWHtZpAokKzEQ6tG1HsNz7CoJWFVAxhnz8YRvQgI9s9GKOhQwGBrbBDWrTj/qhZjGn7F1b80ygbuewcrVgdRGiw7LI/0w/MwP/2aYK+FZfmuRpvhMmTfqEuSxJYUp/hbWo8e0MgI9yrb1SS2OojdD1ltrkVg0Uv4zvC+01hi6COBaKAa5XGb/OAylLg==.mp4",
          "mp4_size": 111927,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YG9GUhudWHtZpAokKzEQ6tG1HsNz7CoJWFVAxhnz8YRvQgI9s9GKOhQwGBrbBDWrTj/qhZjGn7F1b80ygbuewcrtMtcn4a4EatXcs5ZabTRvItyZiHy98BiDjRKz2pmD4QfBvU8R7b6vWbsQGLQHHM4a0vq6wjpEEfNhLER/4NZA.png",
          "apng_size": 330425
        },
        "fixed_width_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YFbnq6WVYlnFlDONyGY8L7uYNAOuU5SYdlr2+/qqRkbFz8FvcmBo9dqx0E5Zzq3z3Ra+fMrvPD0QnP3AYBnYwrnkXvN0dsnkBrQTILP0Zvd9fKwXoSkHQADkEl+drIozVBIIk/NtTgC5yoSWgLSOzpTfZeyx9ICkzazjEiMM1i8q.png",
          "width": 100,
          "height": 100,
          "size": 913
        }
      }
    },
    
    ... more items
  ],
  "meta": {
    "status": 200,
    "msg": "OK"
  },
  "pagination": {
    "total_count": 1,
    "count": 1,
    "offset": 0
  }
}
```

### STICKER Trending Endpoint

Get the latest stickers trending on MojiLaLa with this endpoint. Hand curated by the MojiLaLa editorial team and refreshed daily.  

    https://api.mojilala.com/v1/stickers/trending?api_key=dc6zaTOxFJmzC

[Example](https://api.mojilala.com/v1/stickers/trending?api_key=dc6zaTOxFJmzC&limit=4&fmt=html) trending query with html formatted response.

[Example](https://api.mojilala.com/v1/stickers/trending?api_key=dc6zaTOxFJmzC&limit=4) trending query with default json response.

###### Path

    /v1/stickers/trending

###### Parameters

+ limit - (optional) number of results to return, maximum 100. Default: 25
+ offset - (optional) results offset, defaults to 0);
+ fmt - (optional) return results in html or json format (useful for viewing responses as GIFs to debug/test)
+ rating - limit results to those rated (y,g, pg, pg-13 or r). 
+ lang - (optional) specify default country for regional content; format is 2-letter ISO 639-1 country code. See list of supported langauges [here](#language-support)

### Sample Response: Trending Stickers

```json

{
  "data": [
    {
      "id": "U3RpY2tlci0zODIyOA==",
      "is_animated": true,
      "url": "https://mojilala.com/stickers-emojis/stickers/U3RpY2tlci0zODIyOA==",
      "rating": "g",
      "images": {
        "fixed_height": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYbf5ElQNcjdmUvOwwGuNG7JWee5OcObEL+ve9T30z2OFAhBEaZ4vFzxGEgcrYWg1dy4LPZmkymZP69HuvQILwP.gif",
          "width": 200,
          "height": 200,
          "size": 31585,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYbf5ElQNcjdmUvOwwGuNG7JWee5OcObEL+ve9T30z2OFAhBEaZ4vFzxGEgcrYWg1eOOD0GG3/z9mHn4H35QGgx.webp",
          "webp_size": 14823,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYbf5ElQNcjdmUvOwwGuNG7JWee5OcObEL+ve9T30z2OFAhBEaZ4vFzxGEgcrYWg1eJKS15TmUbDyNyl1AmCAv5.mp4",
          "mp4_size": 4108,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONfZ+hrJrQ6jC7+BwNShdhxy+wmjCislLSSZ/AtC/FZ8FLmKD46I8bfb4rNppSG5u9xrdXBrI4QR5w1KYHCS0W1l.png",
          "apng_size": 31585
        },
        "fixed_height_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbZSzRDS+731zcSgQLY1BkX774hRU/uqyOH7HCVbuoaIEmn6Y0xE0P3yATYA3ZB7jqm+9ZkoUZrxMEqiCtrrmaLh.png",
          "width": 200,
          "height": 200,
          "size": 6968
        },
        "fixed_height_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYEw0lz2gB4shfvNri8Hg/VLIrcFZLcu9DX9UkJmNBLVT2ny7TsUValDvmA9qDNwd8PJXpx5pvjdpB+l/DP8KWcKONMgJ3z55FiVWk7gnbYSg==.gif",
          "width": 200,
          "height": 200,
          "size": 5949,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYEw0lz2gB4shfvNri8Hg/VLIrcFZLcu9DX9UkJmNBLVT2ny7TsUValDvmA9qDNwd8PJXpx5pvjdpB+l/DP8KWc6Ci+KsDmHD++I+2qssCYnA==.webp",
          "webp_size": 3008,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YB9YcHtis7tqRRGmEVgV63dglAjHHN4Yot8oyf4sbZw+SoA2LuUOCkWyyTgINmRW/RjRyWRnOQm0b8/1x7A7NbYEw0lz2gB4shfvNri8Hg/VLIrcFZLcu9DX9UkJmNBLVT2ny7TsUValDvmA9qDNwd8PJXpx5pvjdpB+l/DP8KWcOzEbTqqAd8EB8+Cg0HR+sg==.mp4",
          "mp4_size": 4008,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YLirMGJfCbt4Hlvg7sOCSjPYAQr2X2NDZ6Z2LRihHkiqYkdellmdQP8MKIAlEbEKll8GFbmKsPP09nXfuqRwONeBFerKwDxFXEMSdOfj1Ff2MLqq1iQrliwRZtWAX78o18McJTDPs+SRpfi7ClPMoQYpPanZQZ9ovzhKMvCwzDxP1hLsPtQ+3qW4V7uEXv5R6S7NWTFzRQ3LRezvYTwPLX8=.png",
          "apng_size": 5949
        },
        "fixed_height_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOudTWA3IdyFbS3VXxn0+D3yFKsmDRKSO6OA42Vc5imKPAXgvxylngr+xzybIi4+YTsunK9NOzw5e5m+Z9sKDEPof.gif",
          "width": 320,
          "height": 320,
          "size": 57767,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOudTWA3IdyFbS3VXxn0+D3yFKsmDRKSO6OA42Vc5imKPAXgvxylngr+xzybIi4+YTssdBHUix3szewWGVcTNDItd.webp",
          "webp_size": 28463,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOudTWA3IdyFbS3VXxn0+D3yFKsmDRKSO6OA42Vc5imKPAXgvxylngr+xzybIi4+YTssB+iicGa7e/aVC9yIkcnfS.mp4",
          "mp4_size": 6122,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9ssbylkZSphY+EIRwxu7r2zEFxhmItSkycaj914HNKPqzfqEGoyFvCGY6nPaOxE9QspE95EBy84mKhBiMoX7+U8.png",
          "apng_size": 57767
        },
        "fixed_height_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOudQ+MUlt4UpOyo3agrmZ+EKq1dhQq0ZUPLHjIzKQOZO8xEpm61UAMhe7I0lPdxgFYGNGxl9UY3iIrNPQzl0sopt.png",
          "width": 320,
          "height": 320,
          "size": 13517
        },
        "fixed_height_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOucVck8m9atUiTCkVtXpz0bs9YTSjoyNUFdYRt2xfWfB3mehSsbnV0+YlJkpPaxyyKEgwVvg//B4UFRpdpdbA4aDTgxg3PkO6NvpiCAq/zTGSg==.gif",
          "width": 320,
          "height": 320,
          "size": 11682,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOucVck8m9atUiTCkVtXpz0bs9YTSjoyNUFdYRt2xfWfB3mehSsbnV0+YlJkpPaxyyKEgwVvg//B4UFRpdpdbA4aDkcHL/MLTF7IOJlKXgkwOdw==.webp",
          "webp_size": 5102,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOq3Ds1rfOki8VX/2wnuGgaV2S565pKKPbdgyNkdA3P/QQHLtcQWmfkHAQ7iDaqurBirfsWaAv7l6WqgZrTfOucVck8m9atUiTCkVtXpz0bs9YTSjoyNUFdYRt2xfWfB3mehSsbnV0+YlJkpPaxyyKEgwVvg//B4UFRpdpdbA4aDAeHKBKtEPYDfRYu1EjsMNw==.mp4",
          "mp4_size": 5320,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YBit0FtNC+D721hTfiNMQXqoFdO741WGhpcDzid6RmcV/KhXD47JQBE+e2zwKXX8lw6ayvO+AH3RwLvZkf3In9sy6A/1CEV4wMG6Y9Q+EIoXnFIwXtHXlfPYfM64kp/AZnbBTE848rAsNGT+0ADHrqmn3tqiNMlwJHVNvtUfgwtboqS5MuPOfIkgPk/pJFsLvn5AtOw+ORbAhjSOUUU+FYE=.png",
          "apng_size": 11682
        },
        "fixed_width": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngDg5y3HSelSFYEc0lAyVwkNtiRIk7MOxT/dSWoRP68F6YtVealheDxG+8CZMfF0DTXVM7CZ9l8wIdclQ+6KZqM4.gif",
          "width": 200,
          "height": 200,
          "size": 31585,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngDg5y3HSelSFYEc0lAyVwkNtiRIk7MOxT/dSWoRP68F6YtVealheDxG+8CZMfF0DTVC+RhdF/bWmJx0OKQm/Vtj.webp",
          "webp_size": 14823,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngDg5y3HSelSFYEc0lAyVwkNtiRIk7MOxT/dSWoRP68F6YtVealheDxG+8CZMfF0DTW2kf+4opmiJYvQz5xZ1xY9.mp4",
          "mp4_size": 4108,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVA56BogN9O8x+N7V1le+9LIasAA/fH6/IXgM8vizOwIK0cIA4usZiEY+2oV7WoJz3YI8oy/vBlQ+f2ckZ3EK9+k.png",
          "apng_size": 31585
        },
        "fixed_width_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngA4cI2zKWwhFTccekyJgkzPYp2Yd8L751VsJTh1WY+qpFw2C9Mr+MmU3g31J1F5uZkaZ99Vg00TWYodavYyjeTQ.png",
          "width": 200,
          "height": 200,
          "size": 6968
        },
        "fixed_width_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngBQDbj5uYMKgxYWKbBcnCBCPdIUVhYuQqqmZuV5mxXB2JWbvbpi+xcxZHHykAecUofdqb+rRl4QWKxoUrYFx3fXPjDPqNyQyI5heOIeCaAFDg==.gif",
          "width": 200,
          "height": 200,
          "size": 5949,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngBQDbj5uYMKgxYWKbBcnCBCPdIUVhYuQqqmZuV5mxXB2JWbvbpi+xcxZHHykAecUofdqb+rRl4QWKxoUrYFx3fXoKSrXhBv2Dv2FggYPZfUAg==.webp",
          "webp_size": 3008,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YPj4hc8izR8WkmjJpHKtv0+EYrP4uy+dbZqus3zzt1UQz8H6D7UKrsd/cLnyJgtfyTabbOxaEAoeTZKy+8gpngBQDbj5uYMKgxYWKbBcnCBCPdIUVhYuQqqmZuV5mxXB2JWbvbpi+xcxZHHykAecUofdqb+rRl4QWKxoUrYFx3fXGHDzCb0WoCwCLW+Y+iXdYg==.mp4",
          "mp4_size": 4008,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAc3xWMpZhJtU3TD2L6NjRyMmJP7z6fsBFq5LZ55isu6IReg4VPmC1cux1optHY33E0ELSl6PROFTCusDaKmrVClsADZYSMVzXN47XwnquW/ZjpbwGIC7Db03yKWNyadqTXon1GAMSQXbN6ce23zaKk4GY+z7HwvhqAu+Do0dtIiLFQ+EocXFyFupmkqRRujb4Bjey4XX4HXEv/13IzDSsg=.png",
          "apng_size": 5949
        },
        "fixed_width_medium": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuEoWoUKU+KM0sr++e8uX0mjpFVCVraFdSBOeajk4nYHJZrOwJryo5wQKTJ8oTxa2Y6xrcwPGVb6vNxxqEhslofq.gif",
          "width": 320,
          "height": 320,
          "size": 57767,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuEoWoUKU+KM0sr++e8uX0mjpFVCVraFdSBOeajk4nYHJZrOwJryo5wQKTJ8oTxa2Y5A1HwQ+J0Tyld3YYk2Qflj.webp",
          "webp_size": 28463,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuEoWoUKU+KM0sr++e8uX0mjpFVCVraFdSBOeajk4nYHJZrOwJryo5wQKTJ8oTxa2Y6eBBhtAPsQ4ynRJYgW9Xok.mp4",
          "mp4_size": 6122,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxeJtamMNLDGaijJJjAUbcsJ2I+bevch39Nr3e4jGxOjgjbpqvkZsuN2VfYl7EAp5Qx8eZUK9ETmPnku8ga7rEfl.png",
          "apng_size": 57767
        },
        "fixed_width_medium_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuHpuC9gnb6pnRW2CTCNLNwmsxJWYomQiQMC9QPgfcD+dFLVp51/UfJCEhsTtJgyly0pT3jToia0I6H9VoPjHWp6.png",
          "width": 320,
          "height": 320,
          "size": 13517
        },
        "fixed_width_medium_downsampled": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuFE18duR7aUc2Scnu6PQJB5hRTEs6qtDvSJfusCDie47ElDXGy+LUnIXH2YC5KOfDXu72sLlupWc1OX2qO5THmtcCUrO/tYiQbXyvcAmi2g/A==.gif",
          "width": 320,
          "height": 320,
          "size": 11682,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuFE18duR7aUc2Scnu6PQJB5hRTEs6qtDvSJfusCDie47ElDXGy+LUnIXH2YC5KOfDXu72sLlupWc1OX2qO5THmteM/qtIEWDZrxezFRhjqzaw==.webp",
          "webp_size": 5102,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YAFNWm/paUvLiqYPH3lnFpIGs52wDL+7GQ/hSbFfhOMI9ns1nYCRgegtqxlropGNCfgNBYK5w4qOQa5ja/WWpuFE18duR7aUc2Scnu6PQJB5hRTEs6qtDvSJfusCDie47ElDXGy+LUnIXH2YC5KOfDXu72sLlupWc1OX2qO5THmt6EpZuqeZkSYwa7MuTsRbBQ==.mp4",
          "mp4_size": 5320,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YEn/BHRG13LfRvthgSFzq3H3UdS7374dYpU3w3806tgbfANPm7o+qFyOUpumsaGIKwfltt6ISfATCqpm1wl/xxdJZJ2tMoGSXH5KcYXQK9f4tbW4F1pOe85qCC0+FbfVfyNya4Jw0NCL9Fi6mETYdXomzGlmY7Ghw5NY00txxE37oacQRyqhAny95OblEDFuJ0NvtjyQDyL6NVxRvXo/O9o=.png",
          "apng_size": 11682
        },
        "fixed_height_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YJI9FDU38gx1cczoEc9+3zEciltwmmXXrJxyZDlgpSgerYVIkPx7C9HQlI90tv7WHmakL/UPv1enC/OsWirP1luTRwX05DN8dbCDylURbre+bR6HgWgPqtDietmDQnHbZIZbTx0Y+3qc1epOCmbmyEzAMZIo+6wdJCYx/AosFNgD.gif",
          "width": 100,
          "height": 100,
          "size": 12966,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YJI9FDU38gx1cczoEc9+3zEciltwmmXXrJxyZDlgpSgerYVIkPx7C9HQlI90tv7WHmakL/UPv1enC/OsWirP1luTRwX05DN8dbCDylURbre+bR6HgWgPqtDietmDQnHbZIZbTx0Y+3qc1epOCmbmyEy6tGBgowszH92/J/msfUh5.webp",
          "webp_size": 5372,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YJI9FDU38gx1cczoEc9+3zEciltwmmXXrJxyZDlgpSgerYVIkPx7C9HQlI90tv7WHmakL/UPv1enC/OsWirP1luTRwX05DN8dbCDylURbre+bR6HgWgPqtDietmDQnHbZIZbTx0Y+3qc1epOCmbmyEw/2rEnqk7MpZmDIrgmILxO.mp4",
          "mp4_size": null,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YOT48VSmBWymKmKTfPviwtlHhpIhpFmme+m3apveYfEzzX7VUC36v3D5PCHXHE155H2bHpBegohWaOf5/Glaf53thI9nOd/PI9N3P9oqRs568UW+R02ADBCXMea4jA77lnnS3DmgF9i/bgi+0FqpPWpMo/K5UyWLIQdmrwRTlwfx.png",
          "apng_size": 12966
        },
        "fixed_height_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YJI9FDU38gx1cczoEc9+3zEciltwmmXXrJxyZDlgpSgerYVIkPx7C9HQlI90tv7WHmakL/UPv1enC/OsWirP1lueAFBkn+j/6nOJTj8f5m2Dw5pViKmSi7GW2DifmYpp0JYv7HNNaPa8uIrfjxCToWJ3CE17o6JXDaP8WBhRu+Od.png",
          "width": 100,
          "height": 100,
          "size": 2914
        },
        "fixed_width_small": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YFbnq6WVYlnFlDONyGY8L7uYNAOuU5SYdlr2+/qqRkbFz8FvcmBo9dqx0E5Zzq3z3Ra+fMrvPD0QnP3AYBnYwrkOjY1uK4II73E1/fl+hXtD0wF2hPpUNYLzwAnIO6/+iPtoTrw8jXAJ0PfidYyAiuLcsqJPsD4AQizQawhWjIkc.gif",
          "width": 100,
          "height": 100,
          "size": 12966,
          "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YFbnq6WVYlnFlDONyGY8L7uYNAOuU5SYdlr2+/qqRkbFz8FvcmBo9dqx0E5Zzq3z3Ra+fMrvPD0QnP3AYBnYwrkOjY1uK4II73E1/fl+hXtD0wF2hPpUNYLzwAnIO6/+iPtoTrw8jXAJ0PfidYyAiuLJVIgC9aWkjOY9JQt4+mOv.webp",
          "webp_size": 5372,
          "mp4": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YFbnq6WVYlnFlDONyGY8L7uYNAOuU5SYdlr2+/qqRkbFz8FvcmBo9dqx0E5Zzq3z3Ra+fMrvPD0QnP3AYBnYwrkOjY1uK4II73E1/fl+hXtD0wF2hPpUNYLzwAnIO6/+iPtoTrw8jXAJ0PfidYyAiuIBVutY/QoX7yvoEEX+M7l2.mp4",
          "mp4_size": null,
          "apng": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YG9GUhudWHtZpAokKzEQ6tG1HsNz7CoJWFVAxhnz8YRvQgI9s9GKOhQwGBrbBDWrTj/qhZjGn7F1b80ygbuewcrtMtcn4a4EatXcs5ZabTRvq/7UAilpF/iLXqeX79kDJr4iDDcrs6Ukks2UM5Cxr4f+CPqjitvrVJo4f5qj1B5o.png",
          "apng_size": 12966
        },
        "fixed_width_small_still": {
          "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgD8C/u8sspJO6EKobZnV5YFbnq6WVYlnFlDONyGY8L7uYNAOuU5SYdlr2+/qqRkbFz8FvcmBo9dqx0E5Zzq3z3Ra+fMrvPD0QnP3AYBnYwrlkk/BSa2nPG1XoDqFbgWDQapjKHi+jDspOLFfeQ6RVaX7sP6PrRVDZvRh9I6w3b6v8jfzPGjBAF3L3EvCgoxgk.png",
          "width": 100,
          "height": 100,
          "size": 2914
        }
      }
    },
    
    ... more items
  ],
  "meta": {
    "status": 200,
    "msg": "OK"
  },
  "pagination": {
    "total_count": 3,
    "count": 1,
    "offset": 0
  }
}
```

### STICKER Roulette (Random) Endpoint

Returns a spotaneously selected sticker from MojiLaLa's collection. Optionally limit scope of result to a specific tag. Punctuation will be stripped and ignored. Use a hyphen for phrases. Example [oops](https://api.mojilala.com/v1/stickers/random?api_key=dc6zaTOxFJmzC&tag=oops), [birthday](https://api.mojilala.com/v1/stickers/random?api_key=dc6zaTOxFJmzC&tag=birthday) or [thank-you](https://api.mojilala.com/v1/stickers/random?api_key=dc6zaTOxFJmzC&tag=whatever). Search terms should be URL encoded.
    
    https://api.mojilala.com/v1/stickers/random?api_key=dc6zaTOxFJmzC&tag=oops

[Example](https://api.mojilala.com/v1/stickers/random?api_key=dc6zaTOxFJmzC) random query.

###### Path

    /v1/stickers/random

###### Parameters

+ tag - search query term or phrase
+ rating - limit results to those rated (y,g, pg, pg-13 or r). 
+ fmt - (optional) return results in 'html' or 'json' format (useful for viewing responses as GIFs to debug/test)

###### Sample Reponse: Random

```json
{
  "data": {
    "id": "U3RpY2tlci0yODcyMQ==",
    "is_animated": false,
    "url": "https://mojilala.com/stickers-emojis/stickers/U3RpY2tlci0yODcyMQ==",
    "rating": "g",
    "images": {
      "fixed_height": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHhl1Z6aQsy0uAXUFGg8G+1zlZdfZojGizzabT6CpBup4KK/xlfNDoVAyqfVWGCHGZ.png",
        "width": 180,
        "height": 200,
        "size": 33339,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHhl1Z6aQsy0uAXUFGg8G+1zlZdfZojGizzabT6CpBup5i7IFGqqvDR0/ddF9gLP3i.webp",
        "webp_size": 9794
      },
      "fixed_height_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+Tl3cKgp6aYiJDVYLMWxSzHhl1Z6aQsy0uAXUFGg8G+1zlZdfZojGizzabT6CpBup4KK/xlfNDoVAyqfVWGCHGZ.png",
        "width": 180,
        "height": 200,
        "size": 33339
      },
      "fixed_height_downsampled": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+RaiEzRmYcHFZb2Jxvh0O7WD5BudBBqlpPKC9aGGwZoKpEOPGHAkwS77e7Z/dquW4PaG97aVYGpP951gxZTsSnTcykIDlh0+udPMrZi+PL2/Q==.png",
        "width": 180,
        "height": 200,
        "size": 9527,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOmJ5b9ULthVkcnl4onk3CURWecsV7twYmNhGPZQadCGipDXhaz3/eQZDj4LAIxk6WBrmBv+1RX3DFG047x+RW+RaiEzRmYcHFZb2Jxvh0O7WD5BudBBqlpPKC9aGGwZoKpEOPGHAkwS77e7Z/dquW4PaG97aVYGpP951gxZTsSnTXZ4ot6JZX4o8NcnYtb4WLw==.webp",
        "webp_size": 8462
      },
      "fixed_height_medium": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxS8y6cFuroX7haeSN7CxUBu81c/aDRbGObi1eQqHcFRxFbqwWeCF7ib3XRzYq0gj7.png",
        "width": 288,
        "height": 320,
        "size": 69290,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxS8y6cFuroX7haeSN7CxUBu81c/aDRbGObi1eQqHcFRzJOJCjT/yYZSTvBTYJdFNl.webp",
        "webp_size": 17242
      },
      "fixed_height_medium_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPsJ68AaZB5ceJZm+u8YyHQxS8y6cFuroX7haeSN7CxUBu81c/aDRbGObi1eQqHcFRxFbqwWeCF7ib3XRzYq0gj7.png",
        "width": 288,
        "height": 320,
        "size": 69290
      },
      "fixed_height_medium_downsampled": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPuW2taGunGdgT31tffeBrV6j4ur+863+0VZsDRpujopIYolkUxARA4IlS13VU3JtRnqgZfr+s6ffX1XQB1j5tEUhrk1JyYd+YzUq7lOGjY34w==.png",
        "width": 288,
        "height": 320,
        "size": 20602,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOt3Ff8EqfROXHWN87mZxjPtqjb0shv3P6LYskkT4vGGiYlL+Vr5pqns7GawJ/RUXFDJA3SBbK+4acp6PAHVPKPuW2taGunGdgT31tffeBrV6j4ur+863+0VZsDRpujopIYolkUxARA4IlS13VU3JtRnqgZfr+s6ffX1XQB1j5tEUERzzSFDdevffHzskQZ2Ybg==.webp",
        "webp_size": 14976
      },
      "fixed_width": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qCrNSqW03Vn/IhUMcv+pM4FQnSZZvOimFTk+ggA/87waKqRIbm4A18UzUJWNNHvyh.png",
        "width": 200,
        "height": 222,
        "size": 39180,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qCrNSqW03Vn/IhUMcv+pM4FQnSZZvOimFTk+ggA/87wY/AA9sKjpTwDihiJ0rKcNF.webp",
        "webp_size": 11128
      },
      "fixed_width_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRaj8gQWnzU5VfMZhn73Yt2qCrNSqW03Vn/IhUMcv+pM4FQnSZZvOimFTk+ggA/87waKqRIbm4A18UzUJWNNHvyh.png",
        "width": 200,
        "height": 222,
        "size": 39180
      },
      "fixed_width_downsampled": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRbAieyt2gaeQZV+BtprejzCcNPObVFDr10Pl4K43nzelYbVOmP2mU72J6KOqFgN3x/UxTwAawXadUKx/+MV+wQwNQzouL6L+pJY4lqUvdlCdA==.png",
        "width": 200,
        "height": 222,
        "size": 11030,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgaEOWXEMwgCRvHVhMmE+vRUA+v5rrzYZdEjVTqXGANT8hdZvX7mMfBl/KPTlykXocPxBnTYNMKuMUaGEzjMGRbAieyt2gaeQZV+BtprejzCcNPObVFDr10Pl4K43nzelYbVOmP2mU72J6KOqFgN3x/UxTwAawXadUKx/+MV+wQwpgzZi1UfqPGz48oDD+cvlA==.webp",
        "webp_size": 9752
      },
      "fixed_width_medium": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZCleNKp3f0zXMbcJQ2PU1lKRbd/jo0IQiRUna2fszEX4vC27hgqlRRVHMl5vjB5XeXQ.png",
        "width": 320,
        "height": 355,
        "size": 81346,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZCleNKp3f0zXMbcJQ2PU1lKRbd/jo0IQiRUna2fszEX4vAgOqePwPFa3qtqQ0/iGoXX.webp",
        "webp_size": 19358
      },
      "fixed_width_medium_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFwe6mdkPts13fHvxaWKsZCleNKp3f0zXMbcJQ2PU1lKRbd/jo0IQiRUna2fszEX4vC27hgqlRRVHMl5vjB5XeXQ.png",
        "width": 320,
        "height": 355,
        "size": 81346
      },
      "fixed_width_medium_downsampled": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFzkASGBnQRFtf0AaxcOkX2PCFQ32bqFaRpYgDPjWDlipkysApgbtQjjkRYf06aDf4aDUWv9t9/JU910HQIgAo7fcSLw5O/ks6VUztFfP5CGew==.png",
        "width": 320,
        "height": 355,
        "size": 23102,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOrNWZqMyga6bpqfjuc/nD5B9Bcb8py16p4VYpeQTzMKOO34AqgUyBvKV8bLAOgFPrcD3PPL+LtxIKEElC/f2iFzkASGBnQRFtf0AaxcOkX2PCFQ32bqFaRpYgDPjWDlipkysApgbtQjjkRYf06aDf4aDUWv9t9/JU910HQIgAo7fujl7T8aT3YUmbykJkrFsvw==.webp",
        "webp_size": 16810
      },
      "fixed_height_small": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3n1jVK5CpNEmvro2wJeAOlHXq0DzA9n3Kr1DaTWSpUrtxJNidbNTJK0vALcv1V6xv.png",
        "width": 90,
        "height": 100,
        "size": 11683,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3n1jVK5CpNEmvro2wJeAOlHXq0DzA9n3Kr1DaTWSpUrtmCB2TX91h5fsHZKvP4a1X.webp",
        "webp_size": 4124
      },
      "fixed_height_small_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOvs3XMsXlaNgSlZTqaaD3SrxB2bWtN+AVuOaMhpWucIk+HdCHQqNdAtVVXzHkinHqvx3MbqFxuXqFNobWrVQCU59P4hQAsG8cy5YpiTZcWU3n1jVK5CpNEmvro2wJeAOlHXq0DzA9n3Kr1DaTWSpUrtxJNidbNTJK0vALcv1V6xv.png",
        "width": 90,
        "height": 100,
        "size": 11683
      },
      "fixed_width_small": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZXwRZzY0GTtZfysi5GSFkDbNRAHntTWsUnlUkvDd8cw/nryesz1xWIbCDRZPDsoqm.png",
        "width": 100,
        "height": 111,
        "size": 13724,
        "webp": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZXwRZzY0GTtZfysi5GSFkDbNRAHntTWsUnlUkvDd8cw/a3N6t1SMJY1xFz/WpFmSO.webp",
        "webp_size": 4636
      },
      "fixed_width_small_still": {
        "url": "https://cdn-stickers.mojilala.com/cld/TBGQRb41szec8ZOo8+IQNAZKz59OMLUv5XOuOCAwRoUCNq4wW6eQBtlXmY2hhHxgIxJWHiPKFSMFakOAk9AAOgYiUbPtE6vo1EjcFucR5AAE9pjiimVssJUjoroe0aJP6Y+rfRkNDZBzT+rnUWEWAcYg9zP5vR8ogezDyU1xg77WcjsmP6uWTi8s35l1dljZXwRZzY0GTtZfysi5GSFkDbNRAHntTWsUnlUkvDd8cw/nryesz1xWIbCDRZPDsoqm.png",
        "width": 100,
        "height": 111,
        "size": 13724
      }
    }
  },
  "meta": {
    "status": 200,
    "msg": "OK"
  }
}
```

**Once you are ready to use the MojiLaLa STICKER API in production**, please visit [api.mojilala.com/submit](https://api.mojilala.com/submit) to request a unique API key. As per our section 5 A of our terms of service, we require all apps that use the MojiLaLa API to conspicuously display "Powered By MojiLaLa" attribution marks where the API is utilized. You can find approved official logo marks [here](http://mojilala.com/press-kit-keyboard/).

## Code Examples

Below are code samples in Python, JavaScript, Ruby, PHP and the command line on connecting to the API to make a search query for "happy easter".


#### Python scripting language

```python
# python
import urllib,json
data = json.loads(urllib.urlopen("https://api.mojilala.com/v1/stickers/search?q=happy+easter&api_key=dc6zaTOxFJmzC&limit=5").read())
print json.dumps(data, sort_keys=True, indent=4)
```


#### JavaScript scripting language

```javascript
#javascript, jQuery
var xhr = $.get("https://api.mojilala.com/v1/stickers/search?q=happy+easter&api_key=dc6zaTOxFJmzC&limit=5");
xhr.done(function(data) { console.log("success got data", data); });
```


#### Ruby scripting language

```ruby
#ruby
require 'net/http'
require 'json'
url = "https://api.mojilala.com/v1/stickers/search?q=happy+easter&api_key=dc6zaTOxFJmzC&limit=5"
resp = Net::HTTP.get_response(URI.parse(url))
buffer = resp.body
result = JSON.parse(buffer) 
puts result 
```


#### PHP scripting language

```php
// php
$url = "https://api.mojilala.com/v1/stickers/search?q=happy+easter&api_key=dc6zaTOxFJmzC&limit=5";
print_r(json_decode(file_get_contents($url)));
```


#### Command line, cURL

    # curl, command line
    curl "https://api.mojilala.com/v1/stickers/search?q=happy+easter&api_key=dc6zaTOxFJmzC&limit=5"
    
## Rendition Guide

+ <b>fixed_height</b> - Height set to 200px. Good for mobile use.
+ <b>fixed_height_still</b> - Static preview image for fixed_height
+ <b>fixed_height_downsampled</b> - Height set to 200px. Reduced to 6 frames to minimize file size to the lowest. Works well for unlimited scroll on mobile and as animated previews. See mojilala.com on mobile web as an example.
+ <b>fixed_width</b> - Width set to 200px. Good for mobile use.
+ <b>fixed_width_still</b> - Static preview image for fixed_width
+ <b>fixed_width_downsampled</b> - Width set to 200px. Reduced to 6 frames. Works well for unlimited scroll on mobile and as animated previews.
+ <b>fixed_height_small</b> - Height set to 100px. Good for mobile keyboards.
+ <b>fixed_height_small_still</b> - Static preview image for fixed_height_small
+ <b>fixed_width_small</b> - Width set to 100px. Good for mobile keyboards
+ <b>fixed_width_small_still</b> - Static preview image for fixed_width_small 

## Language Support

The MojiLaLa API offers language support across the Search and Trendind APIs.

	https://api.mojilala.com/v1/stickers/search?q=amor&api_key=dc6zaTOxFJmzC&lang=es

[Example](https://api.mojilala.com/v1/stickers/search?q=amor&api_key=dc6zaTOxFJmzC&lang=es) search query.

###### Parameter

+ lang - specify default language for regional content; format is 2-letter ISO 639-1 country code

### Supported Languages

+ Chinese (Simplified) (zh-Hans)
+ Chinese (Traditional) (zh-Hant)
+ Danish (da)
+ Dutch (nl)
+ English (en)
+ Finnish (fi)
+ French (fr)
+ German (de)
+ Greek (el)
+ Indonesian (id)
+ Italian (it)
+ Japanese (ja)
+ Korean (ko)
+ Malaysian (ms)
+ Norwegian (no)
+ Portuguese (pt)
+ Russian (ru)
+ Spanish (es)
+ Swedish (sv)
+ Thai (th)
+ Turkish (tr)
+ Vietnamese (vi)
+ Arabic (ar)
+ Bosnian (bs)
+ Serbian (sr)
+ Slovak (sk)
+ Slovenian (sl)
+ Afrikaans (af)

Inspired by Giphy API https://github.com/Giphy/GiphyAPI

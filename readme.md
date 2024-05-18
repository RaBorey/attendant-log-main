API List:

1- POST: http://127.0.0.1:8000/api/mobile/auth?email=emp1@coco.com&password=12345678

```
{
    "data": {
        "id": 4,
        "name": "Employee1",
        "email": "emp1@coco.com",
        "role": "user",
        "verified": false,
        "created_at": "2021-11-05T06:30:20.000000Z",
        "updated_at": "2021-11-05T06:30:20.000000Z"
    },
    "token": {
        "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiIzIiwianRpIjoiMTQxN2E4NDBiNzFlMWE4NDc0ZjhkZGY5YzFiMzI4N2FlZmUzZDAwNDBlZjc0OTBkMDVlYzgyMDEyNWU3YTdkMTE3MTZmOGNjY2IzNDkzOTkiLCJpYXQiOjE2MzYxMDA2NTAuNTAwMDU0LCJuYmYiOjE2MzYxMDA2NTAuNTAwMDU5LCJleHAiOjE2Njc2MzY2NTAuNDg0NTExLCJzdWIiOiI0Iiwic2NvcGVzIjpbXX0.Z2BwTLnC0qN5fz5n-xihyvXOPKotVA6lDl8FmBEURD1vYlBST9UQwsEDuuB8DpWpnrLlwbixff0uqfSDYWgHCcScrcMIhstJghEPiHcS9ysBZlrtLPdEA_vG6phcWZPfxKEpkUby3ybHoTjyWZ-9jFRy1zQNJWEP_6RjDnQRdS_IGxKXbD1E544EfIAFKXu_WTIlbwDEtVcha_Eg8Dqp1Xlrpzx0vjC06MQOgr1wWyuMswaZDgoLcK_YzoMxiJDdWwuLCNOhzlSdEOvICzUwVzr6tDbH66qAVk8p0cggjv_NB-nxSw3UvccGp-v5Z_UKd8Q79GOpmtm60TQqx2biZi6O1J1l1WqNxtipw08rk0GK8HeZs9tpJ-wYDPAHs1keDYo3JtPFOXMhKjbKWFdCPC5uSSLjo_eCJTrl3LZ2uxSgebtYlgMV8JdZ4Jlmas_SqVP2rmzYQam9nlTCtE7iKwvGgxeBSCv3F_R-DAovqUGuLBPFN33VdUzNxq1O_q27SHc34wuo6bkz87_-urpgdZ79NCO04-4GoXd789Nyv8pryaAbAL_T9XL6uHgGQxtV9GtDRsaRyPB0teUk-j8xzw53cnNIwdEdwJevajV8CrFDRUOJNRSEdImnO94pnKxU4NVNvIPqwVb4oNeuswqvjYoRM6x19aSQBpvFhK0SxKU",
        "token_type": "Bearer",
        "expires_in": "2022-11-05 08:24:10"
    },
    "message": "Success",
    "statusCode": 200
}
```

2- GET: http://127.0.0.1:8000/api/mobile/list-attendant

```
{
    "data": [
        {
            "id": 1,
            "created_at": "2021-11-05T09:33:21.000000Z",
            "updated_at": "2021-11-05T09:33:21.000000Z",
            "att_date": "2021-11-05 09:33:21",
            "att_clock_type": 1,
            "att_type": 1,
            "user_id": 4,
            "att_latitude": "11.563584",
            "att_longtitude": "104.911654",
            "user": {
                "id": 4,
                "name": "Employee1",
                "email": "emp1@coco.com",
                "role": "user",
                "email_verified_at": null,
                "created_at": "2021-11-05T06:30:20.000000Z",
                "updated_at": "2021-11-05T06:30:20.000000Z"
            }
        },
        {
            "id": 2,
            "created_at": "2021-11-05T09:33:47.000000Z",
            "updated_at": "2021-11-05T09:33:47.000000Z",
            "att_date": "2021-11-05 09:33:47",
            "att_clock_type": 2,
            "att_type": 1,
            "user_id": 4,
            "att_latitude": "11.563584",
            "att_longtitude": "104.911654",
            "user": {
                "id": 4,
                "name": "Employee1",
                "email": "emp1@coco.com",
                "role": "user",
                "email_verified_at": null,
                "created_at": "2021-11-05T06:30:20.000000Z",
                "updated_at": "2021-11-05T06:30:20.000000Z"
            }
        }
    ]
}
```


2- POST: http://127.0.0.1:8000/api/mobile/log-attendant
```
FORM DATA
==============
att_clock_type:1
att_type:2
att_latitude:11.563584
att_longtitude:104.911654
```

MORNING_IN: {"att_clock_type":1, "att_type":1, "att_latitude": "11.563584", "att_longtitude": "104.911654"}
MORNING_OUT: {"att_clock_type":2, "att_type":1, "att_latitude": "11.563584", "att_longtitude": "104.911654"}
AFTERNOON_IN: {"att_clock_type":1, "att_type":2, "att_latitude": "11.563584", "att_longtitude": "104.911654"}
AFTERNOON_OUT: {"att_clock_type":2, "att_type":2, "att_latitude": "11.563584", "att_longtitude": "104.911654"}
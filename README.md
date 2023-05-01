# Pathao-courier-api

API DOCS: [Pathao Api](https://merchant.pathao.com/courier/developer-api)

Python wrapper for Pathao courier api
## Setup


```python
from pathao_api import PathaoApi
```


```python
client = PathaoApi(client_id = 267,
                   client_secret='wRcaibZkUdSNz2EI9ZyuXLlNrnAv0TdPUPXMnD39',
                   username='test@pathao.com',
                   password='lovePathao',
    base_url='https://hermes-api.p-stageenv.xyz')
```

### Test Access Token


```python
client.access_token
```




    'eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjVjMjliMmM4ZmRjNDYyNzliNjgwYTNmYTRiM2E1NjczZDkxYTRmODQ0MGY0MjJmMmVkOGQ3YmIzMDI0MTBmYmVhNjM1MjEyZmE0ZWY2MmY0In0.eyJhdWQiOiIyNjciLCJqdGkiOiI1YzI5YjJjOGZkYzQ2Mjc5YjY4MGEzZmE0YjNhNTY3M2Q5MWE0Zjg0NDBmNDIyZjJlZDhkN2JiMzAyNDEwZmJlYTYzNTIxMmZhNGVmNjJmNCIsImlhdCI6MTY4Mjk0MTcyNSwibmJmIjoxNjgyOTQxNzI1LCJleHAiOjE2ODMzNzM3MjQsInN1YiI6IjM1MiIsInNjb3BlcyI6W119.u9ZURoDJEddtJZqqfhUeFregIJEfcEmrBGRHKkm1uWC6d38DQ7DyL2IYpjdsblba1WlwQI9krYblH_38V8kel48fSO6PlXLc6M1LwXnF8FfHU4MNSlIHNVya9FuuunZf1kDFdh4oJZ8X7Cyez-v0-qpyC5MeGHYV9gnSfg18POmafqKsijBPl14BGD40bmJmvxTDsit03kM4H9-Q78ngDPVk4WaIICOyS_ShpNwJxyAIp4XhX-O50e937dBKmFBRTh_jQdYrQKJLJDVTa0mck2qe5B48qVIL1_yQ0-zqPWrOQ-HBZscDk8jl5aGK6E5b4zO71eqj3_yxD94Ip4Po8l5TZw1Gh4y99-M2wOoQR-QFhoEoI3mowQsiPp4UVZD8DmQjH7lbRsj9Us4oAe-6acYsg67kNUzM5wo54bRbYgHTHy057tMpkNZABK_snGx_kfdJXt_vDjqSrAsgj9NZXtrGLx1iZ6EZn_siJxlrq8MQmkrQjaJlAGxKjqWs_iZ4gSKAR7WZ4zrZPDfoO18kL2LxJEoyG1JYzQIusrbTrRCEiSeumUdnXgYKwxrJvCjkcF_8ywhrZ08_YwgZQ7BBH-ThRslZWi-Cxhyqi73lf8X8-i07ILsEd_XFzm_RXZI-DqMAIu7d52PQWEl1lJF3goasTkbHsnXoLKEcicpRdo0'



### Test city, zone, area list


```python
client.get_city_list()
```
    {'data': [{'city_id': 32, 'city_name': 'B. Baria'},
      {'city_id': 52, 'city_name': 'Bagerhat'},
      {'city_id': 62, 'city_name': 'Bandarban '},
      {'city_id': 34, 'city_name': 'Barguna '},
      {'city_id': 17, 'city_name': 'Barisal'},
      ...
      {'city_id': 61, 'city_name': 'Chuadanga'},
      {'city_id': 11, 'city_name': "Cox's Bazar"},
      {'city_id': 5, 'city_name': 'Cumilla'},
      {'city_id': 1, 'city_name': 'Dhaka'},
     ]}




```python
client.get_zone_list(city_id=1)
```
    {'data': [{'zone_id': 1016, 'zone_name': ' Dhamrai , Savar'},
      {'zone_id': 298, 'zone_name': '60 feet'},
      {'zone_id': 52, 'zone_name': 'Adabor'},
      {'zone_id': 300, 'zone_name': 'Aftab Nagar'},
      {'zone_id': 17, 'zone_name': 'Agargaon'},
      {'zone_id': 317, 'zone_name': 'Arambag'},
      {'zone_id': 965, 'zone_name': 'Ashkona'},
      ....
      {'zone_id': 1003, 'zone_name': 'Uttara Sector 18'},
      {'zone_id': 935, 'zone_name': 'Uttara Sector 3'},
      {'zone_id': 936, 'zone_name': 'Uttara Sector 4'},
      {'zone_id': 937, 'zone_name': 'Uttara Sector 5'},
      {'zone_id': 939, 'zone_name': 'Uttara Sector 7'},
      {'zone_id': 946, 'zone_name': 'Uttara Sector 8'},
      {'zone_id': 940, 'zone_name': 'Uttara Sector 9'},
      {'zone_id': 938, 'zone_name': 'Uttara sector 6'},
      {'zone_id': 962, 'zone_name': 'Vatara'},
      {'zone_id': 37, 'zone_name': 'Wari'},
      {'zone_id': 352, 'zone_name': 'kafrul'},
      {'zone_id': 655, 'zone_name': 'kamranggirchar'},
      {'zone_id': 976, 'zone_name': 'shampur'}]}
```python
client.get_area_list(zone_id=4)
```
    {'data': [{'area_id': 47,
       'area_name': ' Road 02',
       'home_delivery_available': True,
       'pickup_available': True},
      {'area_id': 48,
       'area_name': ' Road 03',
       'home_delivery_available': True,
       'pickup_available': True},
      {'area_id': 49,
       'area_name': ' Road 04',
       'home_delivery_available': True,
       'pickup_available': True},
      ...
      {'area_id': 83,
       'area_name': 'Road 119',
       'home_delivery_available': True,
       'pickup_available': True},
      {'area_id': 16440,
       'area_name': 'Spectra covention centre',
       'home_delivery_available': True,
       'pickup_available': True},
      {'area_id': 16444,
       'area_name': 'The Glass house',
       'home_delivery_available': True,
       'pickup_available': True},
      {'area_id': 16443,
       'area_name': 'Zaara convention centre',
       'home_delivery_available': True,
       'pickup_available': True}]}



### Test get stores


```python
client.get_stores()
```




    {'message': 'Store list fetched.',
     'type': 'success',
     'code': 200,
     'data': {'data': [{'store_id': 55876,
        'store_name': 'Uttara Hub',
        'store_address': '53 , Nawabpur Dhaka -1100',
        'is_active': 1,
        'city_id': 1,
        'zone_id': 259,
        'hub_id': 5,
        'is_default_store': False,
        'is_default_return_store': False},
       ...
       {'store_id': 11026,
        'store_name': 'Logistic Company E-desh',
        'store_address': '12 Gausul Azam Avinue, Uttara-13, Dhaka,Bangladesh',
        'is_active': 1,
        'city_id': 1,
        'zone_id': 1,
        'hub_id': 1,
        'is_default_store': False,
        'is_default_return_store': False}],
      'total': 171,
      'current_page': 1,
      'per_page': 1000,
      'total_in_page': 171,
      'last_page': 1,
      'path': 'http://hermes-api.p-stageenv.xyz/aladdin/api/v1/stores',
      'to': 171,
      'from': 1,
      'last_page_url': 'http://hermes-api.p-stageenv.xyz/aladdin/api/v1/stores?page=1',
      'first_page_url': 'http://hermes-api.p-stageenv.xyz/aladdin/api/v1/stores?page=1'}}



### Test delivery cost calculator


```python
client.get_delivery_cost(city_id=1, zone_id=4, delivery_type=48, item_type='2', store_id='55876')
```
    {'price': 60,
     'discount': 0,
     'promo_discount': 0,
     'plan_id': 39,
     'cod_enabled': 0,
     'cod_percentage': 0,
     'additional_charge': 0}



### Test Create Order


```python
client.create_order(store_id='55876', 
                    order_id='Test #1', 
                    sender_name='Sender Name',
                    sender_phone='01717171717', 
                    recipient_name='Customer', 
                    recipient_phone='01717171718', 
                    address='Gulshan Avenue, Road 105',
                    city_id='1',
                    zone_id='4',
                    area_id='105',
                    special_instruction='None',
                    item_quantity='1',
                    item_weight=1,
                    amount_to_collect=1000,
                    item_description='None',
                    delivery_type=48,
                    item_type='2')
```
```
    {'consignment_id': 'DZ010523G674QD',
     'merchant_order_id': 'Test #1',
     'order_status': 'Pending',
     'delivery_fee': 70}
```
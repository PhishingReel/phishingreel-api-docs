Panels
==========

The detections endpoint allows you to retrieve a list of detections for the provided date or today.

.. contents:: Table of contents
    :local:
    :depth: 3

Authentication and authorisation
--------------------------------

Requests to the detections endpoint do not require authentication or authorisation.

Date
~~~~~~

.. http:get:: /api/v1/panels?date=<datestring>
    
    Retrieve all panel detections for the provided date in YYYYMMdd format.

    **Example request**

    .. tabs::

        .. code-tab:: bash

            $ curl https://phishingreel.io/api/v1/panels?date=20200705


Today
~~~~~~

.. http:get:: /api/v1/panels/today
    
    Retrieve all panel detections for the current date.

    **Example request**

    .. tabs::

        .. code-tab:: bash

            $ curl https://phishingreel.io/api/v1/panels/today

    **Example response**
    
    .. sourcecode:: json

        {
            "uuid": "d6f560a2-a7cb-443b-9b37-16a934ab85b8", 
            "detected": 1594939806, 
            "domain": "secure1.store.app.payment2145621.com.lepeutgoyangsay.com", 
            "phish": {
            "panel_url": "https://secure1.store.app.payment2145621.com.lepeutgoyangsay.com/admin/login.php", 
            "kit": "16Shop", 
            "emails": [
                "maling.missqueen@yandex.com", 
                "admin@16shop.us"
            ]
            }, 
            "host": {
            "ip": "146.148.71.186", 
            "asn": "15169", 
            "owner": "GOOGLE, US", 
            "country": "US"
            }, 
            "certificate": {
            "issued": 1594939559, 
            "ca": "ZeroSSL RSA Domain Secure Site CA", 
            "fingerprint": "46:CE:52:B8:E6:26:35:D8:DA:F5:F7:68:44:52:7A:B3:98:93:93:E0"
            }
        }



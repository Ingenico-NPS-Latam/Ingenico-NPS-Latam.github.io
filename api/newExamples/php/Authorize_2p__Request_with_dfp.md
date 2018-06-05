use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDERX1466Xz-3',
    'psp_MerchOrderId' => 'ORDERX1466Xz',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1912',
    'psp_CustomerAdditionalDetails' => array(
        'DeviceFingerPrint' => '0500xZNak4roiBWb4lG+9HYs7017Cdgd4qQJSmpMrJOB1KvS/OVuOxpO/HxiNDjp6MqUV69yGXIVu
                                wo4cvAVkCKZJcfYG3hMpGlM4Y9SBeoD4p5sZLzz49aklQvps11ulJjBaVF6H91abkfSeaq0iXWZbK
                                ggEl6BXH1X0SK9IQHD1zhBwTfw1vesPcvy58JWfiZ8zzzFq6nnLRu2172JvR+JwB1xFY2IeLKVj1Q
                                S9LZHDDZlE0iTWx+GL+RwrAgiYzyXk8oxUAvMo9PZiCtkSTF2pQXLWvIqAHJLaqhWHbkkfiZiawrt
                                eDWG5fRLHnTznciX7bRPhjavYWJMiRKn2Ug2LwQH1e+Z6dKlqG4saiAu0GFpCgYU4txcXHQfxdOrW
                                wIQdm+BhA1DgdtxocBcStgViMroNzbc4EyycWGgHr8cR0tfLDx+x9i5+XvHiC3L0hMkR9akAOIYWE
                                ulLYO/8TkNVXFplBpFkd1PxbamlzMYVViDr7XpLUelYQ6DjeEk9awB44oHKCiSVF5++JzF6K+FBna
                                Lslv2i2xScO789Tk3Ey2Qm9iedRNrLSH74gK7u9+9h0hAC688dsPZq94fVZe04a5KOFI0JfjvUt/5
                                xAYnQqs2FAqPc98sJ0cjn+K9R5x01jSN93WoYG8uL+N4AOoHQ6m6cuJb/yF6F5Kp3ujJ+504zy93L
                                D2YOEIPTSe+UOkHiZksyHh2+axkAroD6XUQOdLr2jMO37h9ICHpfPGa9bqb28VosXh8aNb4skA9jD
                                ZYTg2hfbipmKqbY3H6hoSc6gsY37GgXAVzAhUB0siTdZAoYZvuKmSw1wyEEJgey+T3JBlseLugg0e
                                mFwfJAhD0aDjYgAZcKrwJ5vb9QMr7rw0m6qXTCMiYq4xTR9qbaA9ztqSRnBtDJ8pghqxpWGDt/aJX
                                cL/2UFF0QYoeIaatkTs1NRZWDxwJ2y6I5AjYqRIcUYB92nZMw7rLIxf1Zdr9OibHWtG1pKxTYh/vA
                                oQSo7fMl4aBSO/SgOTQISO9Hyec5mfLwH6Dmbgjr/zi/E9JPhPDnVenE/eWDgADcAxiA6xD4B5zWv
                                BI4pInjfPtweTB6lHWEAtz131hpLRpaoIpBXMxuOPR3gpFExRkOsVweiqrs7pU6O9WFcLOpsZVEq/
                                czc5mxmXrO8fcrlYF1NNokmqFfY79jEJtxA3nAitC/4BYYTomIMwZ/FeC19n2FTZVRUn1ghrr5QSy
                                jYk6H+R1EIwouzfJi1Z7fC74PE+E6y/O8fJWeDJCPxs2aU4UKLZvcUS6WmDJGtnwnRVGBSM/cxc3U
                                j9x78kfJfDWnhvspuax077cdVZcg5FzcxhMkdk/46ZaXgGmqyKyYWXmGs4YE5j8advR0vxAV
                                bWzh7zzGy7bJ3VReAYpeQBRn7/8tJpm/+PjNPs6tkXb7TqODtdqmpEH62ab5CeQzZtPjCz2qeA3/g
                                bA6jsg/ONxmKFZWsWCmV3A9q5M5IoXgoPj4mWvDxhqFzv9QscAeMhhJkaQyhFko2SFtcEyvaGzkNZ
                                Yh/T+Oh99xuwstNNBHTNWw7HjJo/eQwYt1V1Ola+LoqG95WneoumWX3wLbzP5oRpqXu138RH5CYtw
                                9QQegaS7pmF9X36svIXmTph/4bKBk/D5/TfV8+10VFqkgKjKoeUB/Vl4OChSAwHwjxfN3TowmXJxl
                                IAlSUWBU9oKEX1Gg5xyQxqTPy/jdN53PLhkH7GmZB1KjfTJJ/UCcFPF4WU88iJQ6wm4u7LxzOvfKI
                                rtzdU/lnZofZDnsesY/CQeZUAdUwFmyHagiXqlb4HYxQOR8a1qEOraDu3HPwxsA/m3zamCiHBa054
                                g5KUbvf5U4Y4aIbfQHlD5RE5VNsxydiGaF1JpFb4inDnR7yaL/K1amrt4Y59RWqk9gzFYc57uWQRL
                                MJYKFDx0u4NacMhdibuDwGlbtTyzKXYm2527vKXGHILLTlSkmnsZrruG5TIH8nqFRw4jeEFAmiAgv
                                htC7hIYAy9BVXkKF7H9iMf33OSZYATgZyK/3i8UszuyOEVc89oGNhD5QNzIKaQoyBfhiIhuL+izHL
                                c1KsYN9Ug8VXyrvmjfSGSETeveb0mMVaGiBBCO7b6vCtYHiS6oaG58JYq0PLkkck7W9Mfgw7Fx4hP
                                Af23xffcSwoo2LzClXqw1Ww5xGUy74SHzWn8B9QrC1JfEdLSuBPIKC3UwyMPJ7sa8QShQJF0='
    ),
    'psp_PosDateTime' => '2019-12-01 12:00:00'
);

try{ 
    $response = $sdk->authorize2p($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 

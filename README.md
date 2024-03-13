# 1.8-DUSK-UPDATE



```shell
curl --proto '=https' --tlsv1.2 -sSfL https://github.com/dusk-network/itn-installer/releases/download/v0.1.8/itn-installer.sh | sudo sh
```

```shell
service rusk start
```

- Blokları kontrol edin

```shell
ruskquery block-height
```
Bu şekilde bir çıktı almalısınız

![image](https://github.com/Volkan081/1.8-DUSK-UPDATE/assets/95221293/0d51fefb-41d1-43b9-84af-ce32ebbc7a79)




```shell
tail -F /var/log/rusk.log
```

- Bu şekilde bir çıktı almalısınız
![image](https://github.com/Volkan081/1.8-DUSK-UPDATE/assets/95221293/ccbd3c30-ddd0-4971-abd4-0ca6d51d3e0e)




## Blok kontrol

```shell
curl --location --request POST 'http://127.0.0.1:8080/02/Chain' --header 'Rusk-Version: 0.7.0-rc' --header 'Content-Type: application/json' --data-raw '{
    "topic": "gql",
    "data": "query { block(height: -1) { header { height } } }"
}' | jq '.block.header.height'
```

- bu şekilde çıktı almalısınız

![image](https://github.com/Volkan081/1.8-DUSK-UPDATE/assets/95221293/52bc9cd0-b7e6-4b8a-8241-6b592ef13cd9)




## Stake kontrol

```shell
rusk-wallet stake-info
```

- bu şekilde çıktı almalısınız

![image](https://github.com/Volkan081/1.8-DUSK-UPDATE/assets/95221293/0aa67ee0-e1b9-4c24-9f6c-cdb9eabaf7a6)



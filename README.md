# eth-monitoring

Ethereum monitoring.

Docker Compose example:

    eth-netstatus:
        image: "thbono/eth-netstatus"
        ports:
          - "3000:3000"
        environment:
          PORT: 3000
          WS_SECRET: mysecret

    eth-netapi:
        image: "thbono/eth-netapi"
        environment:
          RPC_HOST: geth
          RPC_PORT: 8545
          INSTANCE_NAME: MyNode
          WS_SERVER: http://eth-netstatus:3000
          WS_SECRET: mysecret

Enjoy it!

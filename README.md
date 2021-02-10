
# maxonrow-benchmark
Maxonrow benchmark tools is used to check the throughput and latency of the maxonrow blockchain. 

### Prerequisites
-- Already started MAXONROW blockchain network by following [maxonrow-go](https://github.com/maxonrow/maxonrow-go/edit/develop/README.md).

## Running Test for BankSend Module of `Maxonrow-benchmark-go` by

1. Compile the relevant go packages

    `make deps`

2. Configure the sender list testing for the `bankSend` module inside the main.go, by example 

    `bank.BankSend([]string{"gohck", "carlo", "mostafa", "nago", "jeansoon", "yk"}, receiverAccList)` 
    
   WHERE this senders must exist inside the `MAXONROW blockchain network` before the network startup.

3. Configure the IP Address for the `bankSend` module inside the bankSend.go, by example 

    `var client = clientrpc.NewJSONRPCClient("http://localhost:26657")` 
    
   WHERE the `localhost` indicate that `MAXONROW blockchain network` was startup in the local HOST.

4. Build the `Maxonrow-benchmark-go`

    `make build`

5. RUN the `Maxonrow-benchmark-go` to interact with `MAXONROW blockchain network`

    `./build/benchmark`


Note: Each time edit the go program, need re-build the whole `Maxonrow-benchmark-go` by clear the path 'build/' and RUN 'make build'.


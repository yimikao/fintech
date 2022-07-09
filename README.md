## Introduction

[Go](https://golang.org) SDK for different Nigerian fintechs. It allows developers inteface with APIs of these companies in their applications.

## Installation 

Run the following command to install Horus on your project:

```bash
go get github.com/yimikao/fintech
```
### Initiate SDK

```go
package main

import github.com/yimikao/fintech/flutterwave

func main() {
    cl, err := flutterwave.New("secret_key")
    if err != nil {
        log.Fatal(err)
    }
    
    ts, _, err := cl.Transaction.GetByID(context.Background(), "transaction_id")
    if err != nil {
        log.Fatal(err)
    }
  
    json.NewEncoder(os.Stdout).Encode(ts)
    
}
```
## Built by 

* Damilola Olayinka - [twitter](https://twitter.com/unimppressed) [GitHub](https://github.com/yimikao)


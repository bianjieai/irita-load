# irita-load

This simple tool is used to execute stress test for IRITA.

## How to use

#### Step.1  Create test accounts and send test-iris to these accounts

1) Copy config.json to $HOME (Set the parameters if necessary)
2) ./irita-load init --config-dir=$HOME

#### Step.2  Sign about tps * duration * 60 TXs, to avoid Sequence Conflict we use 5 different accounts (user0 user1 user2 user3 user4)

./irita-load signtx --config-dir=$HOME --tps=100 --duration=1 --account=user0

#### Step.3   Broadcast tps TXs for every second

./irita-load broadcast --config-dir=$HOME --tps=100

## How to compile
1) dep ensure -v
2) go install

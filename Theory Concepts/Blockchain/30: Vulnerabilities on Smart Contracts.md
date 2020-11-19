# Vulnerabilities on Smart Contracts

- Attack vectors
  - Contract source code
  - Virtual machines
    - Ethereum VM is a distributed stack based machine where all smart contracts are executed
    - Has the following defects
      - Immutable defects
      - Cryptocurrency lost in transfer
      - Bugs in access control
      - Short address attack - accept incorrectly padded arguments

- Front running aka transaction ordering dependence
  - An entity benefits from prior access to privileged market information about upcoming transactions and trades
  - Solutions
    - Batching transactions
    - Precommit schemes

- DoS with block gas limit
  - Prevents attackers from creating an infinite transaction loop
  - Can lead to DoS attacks
    - Unbounded operations'
      - Have a large array of users to pay can max out gas limit
      - Solution is to use a pull-payment system by asking for payment instead of sender initiating
    - Block stuffing
      - Fill several blocks before a transaction and process with a sufficiently high gas price
      - Prevents all other transactions from being processed
    - DoS with unexpected revert
      - Create a fallback function to revert all payments to a bad actor
    - Forcibly sending ether to a contract
    - Insufficient gas griefing
      - Griefing is when a malicious user plays a game in an unintended way to bother other players
      - Used on subcalls
    - Reentracy
      - When a bug in a contract can allow a function to proceed multiple times when it should be prohibited
      - Drain funds
        - Single function reentrancy - same function called recursively
        - Cross function reentrancy - when function shares state with an exploitable function

- Other Vulnerabilities
  - Integer overflow and underflow can break contract execution
  - Timestamp dependence
    - Timestamp manipulation: Miner can edit the timestamp to maximise returns if done within 15 seconds of block validation
    - 15 second rule
    - Floating pragma - Contracts maybe deployed with outdated compilers
    - Function default visibility
    - Outdated compiler version
    - Unchecked call return value
    - Unprotected ether withdrawal - bad actors can withdraw all ether from a contract, by misnaming a function
    - Unprotected self destruct instruction
    - State variable default visibility
    - Unitialised storage pointer
    - Assert violation
    - Use of deprecated functions
    - Delegate call to untrusted callee
    - Signature malleability
    - Incorrect constructor name
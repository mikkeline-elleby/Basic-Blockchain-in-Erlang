# Basic-Blockchain-in-Erlang

# How to run the program:

`erl -sname #{name@host} -setcookie #{secret} -s project start #{cli} #{otherName@otherHost} #{NumberofProcesses}`

- #{name@host} is the sname and hostname of the local erlang VM
- #{secret} the shared secret
- #{cli} `true` for running in interactive (CLI) mode, `false` for seeing the automated 'back-end'
- #{otherName@otherHost} is the sname and hostname of the remote (other) erlang node
- #{NumberofProcesses} the # of processes that will mine new blocks, more = the blockchain grows faster and the likelyhood of forks increases

Example (on the same machine):

`erl -sname foo@localhost -setcookie test -s project start true bar@localhost 3`

`erl -sname bar@localhost -setcookie test -s project start false foo@localhost 60`

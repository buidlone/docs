# 🖥 Technical solution

*V1 implementation is under development, the latest changes can be seen on our Github repository* [**LCF protocol implementation**](https://github.com/buidlone/LCF-protocol)

## Dictionary

 📖 **Investment pool factory** - creates investment pools on demand with a certain specified property
 
 📖 **Distribution contract** - the contract that ends up sending asset streams to the Creator's account. In the direct locking model - it will be the "Investment Pool" itself
 
 📖 **Investment pool** - allows investors to invest money during the fundraiser period

 📖 **Successful fundraiser** - total amount of collected investments is more than or equal to soft cap
 
 📖 **Failed fundraiser** - necessary number of investments was not raised in time, investors are eligible for refunds
 
 📖 **Voting period** - a period where investors vote on milestone completion result. This will determine if project funding continues during the next milestone period. During the voting period, a project will still receive funding for the previous milestone
 
 📖 **Termination window** - a short window of time, when the money stream from the contract to the creator address can be terminated, and all leftover funds are instantly transferred to the creator's account. This is necessary to prevent the contract going over its balance and being jailed, thus losing the buffer of funds that were reserved for streaming to Superfluid's 3P system (Patricians, Plebs, Pirates).

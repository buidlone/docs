# 🖥 Technical solution

{% hint style="info" %}
V1 implementation is under development, the latest changes can be seen on our Github repository
{% endhint %}

### LCF protocol implementation

{% embed url="https://github.com/buidlone/LCF-protocol" %}

### Dictionary

* Investment pool factory - creates investment pools on demand with a certain specified properties.
* Distribution contract - the contract that ends up sending asset streams to the Creator's account. In direct locking model - it will be "Investment Pool" itself.
*   Investment pool - allows investors to invest money during the fundraiser period.

    Keeps those funds locked(TBD), distributes them during milestone periods.
* Successful fundraiser - total amount of collected investments is more than or equal to soft cap.
* Failed fundraiser - necessary amount of investments was not raised in time, investors are eligible for refunds.
*   Voting period - a period of time, where investors vote on milestone completion result.

    This will determine if project funding continues during the next milestone period.

    During voting period, project will still receive funding for the previous milestone.
* Termination window - a short window of time, when the money stream from the contract to the creator address can be terminated, and all of the leftover funds are instantly transferred to the creator's account. This is necessary to prevent the contract going over it's balance and being jailed, losing the buffer of funds that was reserved for streaming to Superfluid's 3P system(Patricians, Plebs, Pirates).

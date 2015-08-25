# TwoPhaseLocking
Implementation of rigorous two phase locking protocol for concurrency control with the wait-die method for dealing with deadlock

Design and Implementation of the program:

I have designed two HashMaps for tracking all the transactions and a PriorityQueue to store the waiting transactions. We store the list of all operations in Transaction table (TT) and Lock Table (LT).

TRANSACTION TABLE:
The fields to be stored are,
•	Transaction_ID
•	Transaction_state (active, blocked/waiting, aborted/cancelled, committed)
•	Transaction_timestamp
•	List of items locked by the transaction

Transaction_ID	Transaction_ Timestamp	Trans_State	Items_locked


LOCK TABLE:
The fields to be stored are,
•	Item_name
•	Lock_state(read/share locked, write/exclusive lock)
•	Transaction_id

Item_name	transid_RL	transid_WL	trans_waiting_write	trans_waiting_read


READ_ME.txt

###############

Authors:
Alex King
Manuel Perez

###############
	
	
***LOTTERY SCHEDULER***

-NOTE:
	The scheduler uses a lotteryScheduler() function, a setpriority() function, and a
	inUserQueue() function to implement a lottery scheduler.
	
-lotteryScheduler()
	counts the number of total tickets, then it picks a ticket at
	random and gives the process hilder if the tieckt the highets priority enableling
	the process to run. Thi function gets called within do_noquantum, do_stop_scheduling,
	and do_nice to schedule a new process.
	
-setpriority()
	Adds or subtracts tickets form the toal amount a process holds. A process can never hold
	more than 100 tickets or less than 1. This function gets calle within do_noquantum
	(reduce tickets), do_stop_scheduling (add tickets), and do_nice(adds or reduces tickets
	according to intended priority).
		
-inUserQueue()
	checks to see that the specified prcess is within the user Queue. This function is used
	in several calls for error checking.
	
	
	
<<<<<<< HEAD
# csd3-continuous-job-demo
A demo script for how to run auto-restarting jobs on the Cambridge CSD3 compute cluster.
=======
# Working example demonstrating how to run never-ending jobs on CSD3

Main logic lives in file demo.py

We launch csd3 by calling ```sbatch slurm_submit.peta4-skylake``` (if you are not paula's student change the billing info obviously) which in turn calls demo.py until it has counted up to some number. The program only lives for 90 seconds, and 60 seconds before termination CSD3 sends a SIGINT signal to the main process which in turn forces it to save whatever the number is that it currently has counted up to, and calls on CSD3 to spawn a new job.
>>>>>>> d165d10 (pushing working version of continuous job demo)

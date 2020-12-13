# Tasks to complete

# Task 1 -- Install a K8S Cron Job
Create a Kubernetes Cronjob with a busybox image that spins up a job every minute that prints
the date every minute in its logs.

# Task 2 -- Pod with secret mounts
Create a secret called “pdsecret" with values var1=foo, var2=bar and
create an nginx pod with a volume nginx-volume which reads data from this
secret pdsecret and mounts it on the path /etc/pd, as well as exports environment variables
VAR1 and VAR2 in the environment. Exec into the pod to confirm VAR1 and VAR2 are in the
environment and that the secret is mounted at /etc/pd

# Task 3 -- Nginx deployment with HPA
Create an nginx deployment with 4 replicas with label my-nginx and expose port 80; then
create the service for this nginx pod with the pod selector app: my-nginx. To verify, port-forward
to your local machine at port 8000 so you can visit http://localhost:8000 and see the nginx
welcome page. Install a HPA that scales when the CPU usage exceeds 25% with a max of 10
replicas.

# Bonus Task
Use helm to install prometheus and grafana on the cluster and install a grafana dashboard to
monitor the kubernetes cluster

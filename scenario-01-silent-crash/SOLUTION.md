# Solution: The Silent Crash

## Symptoms
The Pod remains in a `Pending` state indefinitely and never actually starts the container.

## Diagnosis
Run the following command to check the scheduler's events:
`kubectl describe pods -l app=web`

At the bottom of the output in the **Events** section, you will see a `FailedScheduling` warning:
`Warning  FailedScheduling  default-scheduler  0/1 nodes are available: 1 node(s) didn't match Pod's node affinity/selector.`

## The Fix
The deployment is requesting a node with the label `hardware-type: quantum-computer`. Since no nodes in your cluster have this label, the scheduler cannot place the pod.

To fix it, edit `deploy.yaml` and either remove the entire `nodeSelector` block or change the label to match an existing node in your cluster.

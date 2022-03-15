# Rolling, Canary, Blue-green deployments

**Rolling Deployment**

****

Deployments support updating images to a new version through a rolling update mechanism. When a Deployment is updated with a new version, it creates a new ReplicaSet and slowly increases the number of replicas in the new ReplicaSet as it decreases the replicas in the old ReplicaSet.



In kubernetees, it's done by editing deployment with new version and updating image with latest version of deployment



It possible to pause, resume, rollback new changes with this deployment.

****

**Canary Deployment**

A canary deployment consists of a separate deployment with your new version and a service that targets both your normal, stable deployment as well as your canary deployment. Usually needs a new track version called canary in kubernetees. Also a few deployments are using new version initially.



### Blue-green deployments <a href="#step9" id="step9"></a>

Rolling updates are ideal because they allow you to deploy an application slowly with minimal overhead, minimal performance impact, and minimal downtime. There are instances where it is beneficial to modify the load balancers to point to that new version only after it has been fully deployed. In this case, blue-green deployments are the way to go.

Kubernetes achieves this by creating two separate deployments; one for the old "blue" version and one for the new "green" version. Use your existing `hello` deployment for the "blue" version. The deployments will be accessed via a Service which will act as the router. Once the new "green" version is up and running, you'll switch over to using that version by updating the Service.





**References:**

{% embed url="https://www.cloudskillsboost.google/focuses/639?parent=catalog" %}

{% embed url="https://www.cloudskillsboost.google/focuses/552?parent=catalog" %}

{% embed url="https://martinfowler.com/bliki/CanaryRelease.html" %}

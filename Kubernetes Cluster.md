# Requirements
>## Leader Node
>1. External IP bound to the domain for website
>2. Ssh access (To control Leader node without a physical screen)
>   - Choose another external port to forward to 22 (if password auth is used)
>   - Better solution: Use key pairs (Github keys or similar)
>3. Microk8s (Handles the kubernetes cluster connection seemlessly)
>4. Docker
>5. Internet Access

> ## Worker Nodes
> 1. MicroK8s (Same version across **ALL** devices)
> 2. Docker
> 3. Ssh access to join leader cluster (each worker has his own unique token given from leader)
> 4. Internet access optional (preferred to not be visible on network)

>## Docker Images
>1. (for now) Ebn El Haitham 
>2. Git instance (for private images?)

>## Steps
>1. Install Ubuntu on each device (20.04 or 22.04)
>2. Install MicroK8s and Docker on each device (prompted in installer)
>3. ensure SSH is enabled (Root login disabled)
>4. Connect all "workers" to leader node `microk8s add-node` 
>5. Deploy images (still need to be built)
>6. Deploy load balancer service (YAML premade, just slight modification needed)

>## References
>### MicroK8s
>https://microk8s.io/docs/clustering
>### Docker Images
>https://docs.docker.com/develop/develop-images/baseimages/
>https://docs.docker.com/engine/reference/builder/
>https://www.stereolabs.com/docs/docker/creating-your-image/



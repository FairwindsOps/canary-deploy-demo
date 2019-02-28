# Canary Deployment Demo
This is a very simple example of how canary deployments can work with existing tooling. This utilizes nginx ingress for routing the canary traffic with a specified probability. In this example we require manual approval to go from 10% of traffic to 50% and then finally to 100%.

## Steps Involved
1. Apply new deployment and ingress with canary weight 10
2. Increase canary weight on new deployment to 50
3. Apply stable deployment and ingress
4. Scale down canary deployment and weight for ingress

## Potential Next Steps
Since both the stable and canary deployments are deployed with services targeting them, it would be trivial to configure additional DNS endpoints to target these directly.

## Limitations
This requires both stable and canry deployment configurations to match. A tool like Helm could be used here to simplify templating.
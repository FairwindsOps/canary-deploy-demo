# Canary Deployment Workflow
1. Apply new deployment and ingress with canary weight 10
2. Increase canary weight on new deployment to 50
3. Apply stable deployment and ingress with canary weight 100
4. Delete canary deployment and ingress
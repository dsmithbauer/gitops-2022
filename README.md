# LeidoSphere 2022 - GitOps Demo

## Prerequisites

1. Local cluster
2. Install ArgoCD
3. Get Admin password
   * kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

## Demo

1. Manually add Forked Guestbook Example
   * Show manual increase of replicas
   * Show rollback using previous Git SHA

2. Show ECK Operator Helm App

3. Install Elastic Search and Kibana from Yaml
   * Port forward
   * User: elastic
   * Password:
     * kubectl get secret quickstart-es-elastic-user -o=jsonpath='{.data.elastic}' | base64 --decode; echo

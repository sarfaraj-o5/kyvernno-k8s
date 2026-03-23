Installing Kyverno CLI for debugging policies
To install the Kyverno CLI, follow these steps:

Using Homebrew (macOS & Linux)
brew install kyverno
Using a Precompiled Binary (Linux & macOS)
curl -LO https://github.com/kyverno/kyverno/releases/latest/download/kyverno-linux-amd64.tar.gz
tar -xvf kyverno-linux-amd64.tar.gz
sudo mv kyverno /usr/local/bin/
Verify Installation
kyverno version

Checking Blocked Requests in Kyverno
To see if a request is blocked by Kyverno

Kyverno Admission Controller Logs
kubectl logs -n kyverno -l app.kubernetes.io/name=kyverno -f

## Audit Events in k8s
kubectl get events --all-namespaces | grep kyverno

## kyverno policy repots
kubectl get clusterpolicyreport
kubectl get policyreport -o yaml

Using Webhooks for Real-Time Policy Enforcement

Kyverno uses webhooks to intercept API requests in Kubernetes. Administrators can monitor webhook logs to check which requests were blocked or modified.

kubectl logs -l kyverno=kyverno -n kyverno 

## kyverno CLI for local testing
kyverno apply policy.yaml --resource=resource.yaml
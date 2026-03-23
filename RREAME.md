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

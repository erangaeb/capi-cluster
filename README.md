# create kind cluster
kind create cluster --config cluster-config.yaml --name mgmt --image kindest/node:v1.23.10

# setup cluster api
export CLUSTER_TOPOLOGY=true
clusterctl init --infrastructure docker

# Makefile to deploy KDP operator to a k8s cluster

.PHONY: deploy up down destroy uninstall

.DEFAULT_GOAL := deploy

# Deploy kdp-operator to the cluster
deploy:
	kubectl apply -f ../../yaml/operator/namespace.yaml
	kubectl apply -f ../../yaml/operator/crd.yaml
	kubectl apply -f ../../yaml/operator/rbac.yaml
	kubectl apply -f ../../yaml/operator/deployment.yaml

up: deploy # alias

# Remove kdp-operator from the cluster
destroy:
	kubectl delete -f ../../yaml/operator/namespace.yaml
	kubectl delete -f ../../yaml/operator/crd.yaml
	kubectl delete -f ../../yaml/operator/rbac.yaml
	kubectl delete -f ../../yaml/operator/deployment.yaml

down: destroy # alias
uninstall: destroy # alias
# generate cert & key
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes
	# Common Name: secure-ingress.com


# Complete Example
https://github.com/killer-sh/cks-course-environment/tree/master/course-content/cluster-setup/secure-ingress


# curl command to access, replace your IP and secure NodePort->443
curl https://secure-ingress.com:31047/service2 -kv --resolve secure-ingress.com:31047:34.105.246.174


# k8s docs
https://kubernetes.io/docs/concepts/services-networking/ingress/#tls

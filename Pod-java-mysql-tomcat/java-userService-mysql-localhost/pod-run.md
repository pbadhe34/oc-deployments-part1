pod run


  kubectl  create -f MySql-PersistentVoulme.yml

   kubectl create -f MySql-PersistentVoulme-Claim.yml

   kubectl  create -f user-service-pod-mysql

  kubectl get pods

  kubectl get pod user-service-pod-app -o yaml |grep podIP

   podIP: 172.17.0.6

  kubectl logs user-service-pod-app user-service-app 


  kubectl logs user-service-pod-app mysql-pod

  docker container ls --format "{{.Names}} : {{.Image}}
> "
k8s_mysql-pod_user-service-pod-app_myproject_d0c9eba9-092d-11ea-9786-000c2966b591_0 : mysql

k8s_user-service-app_user-service-pod-app_myproject_d0c9eba9-092d-11ea-9786-000c2966b591_0 : pbadhe34/my-apps

k8s_POD_user-service-pod-app_myproject_d0c9eba9-092d-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_webconsole_webconsole-58f469f8ff-7644z_openshift-web-console_0507e9ab-092d-11ea-9786-000c2966b591_0 : be30b6cce5fa

k8s_POD_webconsole-58f469f8ff-7644z_openshift-web-console_0507e9ab-092d-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_router_router-1-m9lz7_default_f3550539-092c-11ea-9786-000c2966b591_0 : 263246e93606

k8s_registry_docker-registry-1-zxhg5_default_f354806a-092c-11ea-9786-000c2966b591_0 : 9dffb2abf1dd

k8s_POD_router-1-m9lz7_default_f3550539-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_POD_docker-registry-1-zxhg5_default_f354806a-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_operator_openshift-web-console-operator-664b974ff5-9lhcc_openshift-core-operators_e8f4ebfe-092c-11ea-9786-000c2966b591_0 : openshift/origin-hypershift

k8s_POD_openshift-web-console-operator-664b974ff5-9lhcc_openshift-core-operators_e8f4ebfe-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_c_openshift-controller-manager-bmsfw_openshift-controller-manager_dc0cd648-092c-11ea-9786-000c2966b591_0 : openshift/origin-hypershift

k8s_POD_openshift-controller-manager-bmsfw_openshift-controller-manager_dc0cd648-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_apiserver_openshift-apiserver-g65c8_openshift-apiserver_92727952-092c-11ea-9786-000c2966b591_0 : openshift/origin-hypershift

k8s_POD_openshift-apiserver-g65c8_openshift-apiserver_92727952-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_apiservice-cabundle-injector-controller_apiservice-cabundle-injector-8ffbbb6dc-zqdpn_openshift-service-cert-signer_a25aa89a-092c-11ea-9786-000c2966b591_0 : 47dadf9d43b6

k8s_service-serving-cert-signer-controller_service-serving-cert-signer-668c45d5f-9v87g_openshift-service-cert-signer_a0e10af0-092c-11ea-9786-000c2966b591_0 : 47dadf9d43b6

k8s_POD_apiservice-cabundle-injector-8ffbbb6dc-zqdpn_openshift-service-cert-signer_a25aa89a-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_kube-dns_kube-dns-qgp4s_kube-dns_9254d3a9-092c-11ea-9786-000c2966b591_0 : openshift/origin-control-plane

k8s_POD_service-serving-cert-signer-668c45d5f-9v87g_openshift-service-cert-signer_a0e10af0-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_operator_openshift-service-cert-signer-operator-6d477f986b-8m6xn_openshift-core-operators_9254a7b8-092c-11ea-9786-000c2966b591_0 : openshift/origin-service-serving-cert-signer

k8s_kube-proxy_kube-proxy-x5vp4_kube-proxy_925865df-092c-11ea-9786-000c2966b591_0 : openshift/origin-control-plane

k8s_POD_kube-dns-qgp4s_kube-dns_9254d3a9-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_POD_openshift-service-cert-signer-operator-6d477f986b-8m6xn_openshift-core-operators_9254a7b8-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_POD_kube-proxy-x5vp4_kube-proxy_925865df-092c-11ea-9786-000c2966b591_0 : openshift/origin-pod:v3.11

k8s_api_master-api-localhost_kube-system_c53add43bbc8aa484005d2aeeb5dd39c_0 : openshift/origin-hypershift

k8s_etcd_master-etcd-localhost_kube-system_ce1b4f38bbca006b979fa286af1a66cd_0 : openshift/origin-control-plane

k8s_controllers_kube-controller-manager-localhost_kube-system_2d5691e8031e7cd3ff23d43ee7d111c1_0 : openshift/origin-hyperkube

k8s_scheduler_kube-scheduler-localhost_kube-system_2223f71fe0fa2de8e1e3b14244a86d28_0 : openshift/origin-hyperkube

k8s_POD_master-etcd-localhost_kube-system_ce1b4f38bbca006b979fa286af1a66cd_0 : openshift/origin-pod:v3.11

k8s_POD_kube-controller-manager-localhost_kube-system_2d5691e8031e7cd3ff23d43ee7d111c1_0 : openshift/origin-pod:v3.11

k8s_POD_kube-scheduler-localhost_kube-system_2223f71fe0fa2de8e1e3b14244a86d28_0 : openshift/origin-pod:v3.11

k8s_POD_master-api-localhost_kube-system_c53add43bbc8aa484005d2aeeb5dd39c_0 : openshift/origin-pod:v3.11

origin : openshift/origin-node:v3.11





  http://172.17.0.6:8090/users


  oc get pod hello-openshift -o yaml |grep podIP

# Policies

|Name|Rule Types|API Groups|Kinds|Description|
|---|---|---|---|---|
|[Namespace Has Networkpolicy](policy/combine/namespace-has-networkpolicy)|violation|core, networking.k8s.io|Namespace, NetworkPolicy|violation: Check if a Namespace has a networking.k8s.io/v1:NetworkPolicy|
|[Common K8s Labels Notset](policy/ocp/bestpractices/common-k8s-labels-notset)|violation|apps.openshift.io, apps, core, route.openshift.io|DeploymentConfig, DaemonSet, Deployment, StatefulSet, Service, Route|violation: Check if all workload related kinds contain labels as suggested by https://kubernetes.io/docs/concepts/overview/working-with-objects/common-labels|
|[Container Env Maxmemory Notset](policy/ocp/bestpractices/container-env-maxmemory-notset)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have the CONTAINER_MAX_MEMORY env set using the downward api|
|[Container Image Latest](policy/ocp/bestpractices/container-image-latest)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds are not using the latest tag for their image|
|[Container Java Xmx Set](policy/ocp/bestpractices/container-java-xmx-set)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds do not set the Java Xmx option|
|[Container Labelkey Inconsistent](policy/ocp/bestpractices/container-labelkey-inconsistent)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have consistent key names for their labels|
|[Container Liveness Readinessprobe Equal](policy/ocp/bestpractices/container-liveness-readinessprobe-equal)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have not set their probes to be the same|
|[Container Livenessprobe Notset](policy/ocp/bestpractices/container-livenessprobe-notset)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have their liveness prob set|
|[Container Readinessprobe Notset](policy/ocp/bestpractices/container-readinessprobe-notset)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have their readiness prob set|
|[Container Resources Limits Cpu Set](policy/ocp/bestpractices/container-resources-limits-cpu-set)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds do not set limits for CPU|
|[Container Resources Limits Memory Greater Than](policy/ocp/bestpractices/container-resources-limits-memory-greater-than)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds limits for memory is not greater than an upper bound|
|[Container Resources Limits Memory Notset](policy/ocp/bestpractices/container-resources-limits-memory-notset)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds has set their limits for memory|
|[Container Resources Memoryunit Incorrect](policy/ocp/bestpractices/container-resources-memoryunit-incorrect)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds memory limits and requests unit is valid|
|[Container Resources Requests Cpuunit Incorrect](policy/ocp/bestpractices/container-resources-requests-cpuunit-incorrect)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds cpu requests unit is valid|
|[Container Resources Requests Memory Greater Than](policy/ocp/bestpractices/container-resources-requests-memory-greater-than)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds requests for memory is not greater than an upper bound|
|[Container Secret Mounted Envs](policy/ocp/bestpractices/container-secret-mounted-envs)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds do not have secrets mounted as envs|
|[Container Volumemount Inconsistent Path](policy/ocp/bestpractices/container-volumemount-inconsistent-path)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds have consistent paths for their volume mounts|
|[Container Volumemount Missing](policy/ocp/bestpractices/container-volumemount-missing)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds does not specify a volume without a corresponding volume mount|
|[Deploymentconfig Triggers Notset](policy/ocp/bestpractices/deploymentconfig-triggers-notset)|violation|apps.openshift.io|DeploymentConfig|violation: Check if a DeploymentConfig has 'spec.triggers' set|
|[Pod Hostnetwork](policy/ocp/bestpractices/pod-hostnetwork)|violation|apps.openshift.io, apps|DeploymentConfig, DaemonSet, Deployment, StatefulSet|violation: Check workload kinds has 'spec.hostNetwork' set|
|[Pod Replicas Below One](policy/ocp/bestpractices/pod-replicas-below-one)|violation|apps.openshift.io, apps|DeploymentConfig, Deployment|violation: Check workload kinds has replicas <= 1|
|[Pod Replicas Not Odd](policy/ocp/bestpractices/pod-replicas-not-odd)|violation|apps.openshift.io, apps|DeploymentConfig, Deployment|violation: Check workload kinds has replicas not odd|
|[Rolebinding Roleref Apigroup Notset](policy/ocp/bestpractices/rolebinding-roleref-apigroup-notset)|violation|rbac.authorization.k8s.io|RoleBinding|violation: Check if a RoleBinding has 'roleRef.apiGroup' set|
|[Rolebinding Roleref Kind Notset](policy/ocp/bestpractices/rolebinding-roleref-kind-notset)|violation|rbac.authorization.k8s.io|RoleBinding|violation: Check if a RoleBinding has 'roleRef.kind' set|
|[Buildconfig V1](policy/ocp/deprecated/3_11/buildconfig-v1)|violation|v1|BuildConfig|violation: Check for deprecated v1 apiVersion. OCP4.x expects build.openshift.io/v1|
|[Deploymentconfig V1](policy/ocp/deprecated/3_11/deploymentconfig-v1)|violation|v1|DeploymentConfig|violation: Check for deprecated v1 apiVersion. OCP4.x expects apps.openshift.io/v1|
|[Imagestream V1](policy/ocp/deprecated/3_11/imagestream-v1)|violation|v1|ImageStream|violation: Check for deprecated v1 apiVersion. OCP4.x expects image.openshift.io/v1|
|[Projectrequest V1](policy/ocp/deprecated/3_11/projectrequest-v1)|violation|v1|ProjectRequest|violation: Check for deprecated v1 apiVersion. OCP4.x expects project.openshift.io/v1|
|[Rolebinding V1](policy/ocp/deprecated/3_11/rolebinding-v1)|violation|v1|RoleBinding|violation: Check for deprecated v1 apiVersion. OCP4.x expects rbac.authorization.k8s.io/v1|
|[Route V1](policy/ocp/deprecated/3_11/route-v1)|violation|v1|Route|violation: Check for deprecated v1 apiVersion. OCP4.x expects route.openshift.io/v1|
|[Securitycontextconstraints V1](policy/ocp/deprecated/3_11/securitycontextconstraints-v1)|violation|v1|SecurityContextConstraints|violation: Check for deprecated v1 apiVersion. OCP4.x expects security.openshift.io/v1|
|[Template V1](policy/ocp/deprecated/3_11/template-v1)|violation|v1|Template|violation: Check for deprecated v1 apiVersion. OCP4.x expects template.openshift.io/v1|
|[Buildconfig Custom Strategy](policy/ocp/deprecated/4_1/buildconfig-custom-strategy)|violation|build.openshift.io|BuildConfig|violation: Check if 'exposeDockerSocket' is set on a BuildConfig. See: https://docs.openshift.com/container-platform/4.1/release_notes/ocp-4-1-release-notes.html#ocp-41-deprecated-features|
|[Authorization Openshift](policy/ocp/deprecated/4_2/authorization-openshift)|violation|authorization.openshift.io|ClusterRole, ClusterRoleBinding, Role, RoleBinding|violation: Check for deprecated authorization.openshift.io apiVersion. >= OCP4.2 expects rbac.authorization.k8s.io/v1. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Automationbroker V1alpha1](policy/ocp/deprecated/4_2/automationbroker-v1alpha1)|violation|automationbroker.io|Bundle, BundleBinding, BundleInstance|violation: Check for deprecated automationbroker.io/v1alpha1 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Catalogsourceconfigs V1](policy/ocp/deprecated/4_2/catalogsourceconfigs-v1)|violation|operators.coreos.com|CatalogSourceConfigs|violation: Check for deprecated operators.coreos.com/v1 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Catalogsourceconfigs V2](policy/ocp/deprecated/4_2/catalogsourceconfigs-v2)|violation|operators.coreos.com|CatalogSourceConfigs|violation: Check for deprecated operators.coreos.com/v2 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Operatorsources V1](policy/ocp/deprecated/4_2/operatorsources-v1)|violation|operators.coreos.com|OperatorSource|violation: Check for deprecated operators.coreos.com/v1 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Osb V1](policy/ocp/deprecated/4_2/osb-v1)|violation|osb.openshift.io|TemplateServiceBroker, AutomationBroker|violation: Check for deprecated osb.openshift.io/v1 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Servicecatalog V1beta1](policy/ocp/deprecated/4_2/servicecatalog-v1beta1)|violation|servicecatalog.k8s.io|ClusterServiceBroker, ClusterServiceClass, ClusterServicePlan, ServiceInstance, ServiceBinding|violation: Check for deprecated servicecatalog.k8s.io/v1beta1 apiVersion. See: https://docs.openshift.com/container-platform/4.2/release_notes/ocp-4-2-release-notes.html#ocp-4-2-deprecated-features|
|[Buildconfig Jenkinspipeline Strategy](policy/ocp/deprecated/4_3/buildconfig-jenkinspipeline-strategy)|violation|build.openshift.io|BuildConfig|violation: Check if 'jenkinsPipelineStrategy' is set on a BuildConfig. See: https://docs.openshift.com/container-platform/4.3/release_notes/ocp-4-3-release-notes.html#ocp-4-3-deprecated-features|
|[Deployment Has Matching Poddisruptionbudget](policy/ocp/requiresinventory/deployment-has-matching-poddisruptionbudget)|violation|apps|Deployment|violation: Check if a Deployment has a matching policy/v1beta1:PodDisruptionBudget, via 'spec.template.metadata.labels'|
|[Deployment Has Matching Pvc](policy/ocp/requiresinventory/deployment-has-matching-pvc)|violation|apps|Deployment|violation: Check if a Deployment has 'spec.template.spec.volumes.persistentVolumeClaim' set, there is a matching v1:PersistentVolumeClaim|
|[Deployment Has Matching Service](policy/ocp/requiresinventory/deployment-has-matching-service)|violation|apps|Deployment|violation: Check if a Deployment has a matching v1:Service, via 'spec.template.metadata.labels'|
|[Deployment Has Matching Serviceaccount](policy/ocp/requiresinventory/deployment-has-matching-serviceaccount)|violation|apps|Deployment|violation: Check if a Deployment has 'spec.serviceAccountName' set, there is a matching v1:ServiceAccount|
|[Service Has Matching Servicemonitor](policy/ocp/requiresinventory/service-has-matching-servicemonitor)|violation|core|Service|violation: Check if a Service has a matching monitoring.coreos.com/v1:ServiceMonitor, via 'spec.selector'|
|[Contains Layer](policy/podman/history/contains-layer)|violation|redhat-cop.github.com|PodmanHistory|violation: Check the image contains a specific SHA in its history|
|[Image Size Not Greater Than](policy/podman/images/image-size-not-greater-than)|violation|redhat-cop.github.com|PodmanImages|violation: Check the image size is not greater than a specific value|
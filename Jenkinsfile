def serviceName = "training-books-ms"
def registry = "docker-registry:5000"


node("docker") {
    git "https://github.com/cloudbees/${serviceName}.git"
    common.runPreDeploymentTests(serviceName, registry)
    common.build(serviceName, registry)
}

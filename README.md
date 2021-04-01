# Govvy_Jenkins

## Restart Jenkins
```groovy
import jenkins.model.Jenkins
def instance = Jenkins.instance
instance.setCrumbIssuer(null)
```
## Temporarily disable Jenkins CSRF
```groovy
import jenkins.model.Jenkins
def instance = Jenkins.instance
instance.setCrumbIssuer(null)
```
## Enable Jenkins CSRF
```groovy
import hudson.security.csrf.DefaultCrumbIssuer
import jenkins.model.Jenkins
def instance = Jenkins.instance
instance.setCrumbIssuer(new DefaultCrumbIssuer(true))
instance.save()
```

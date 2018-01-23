# About

This Nuxeo Package contains a custom resolver for Okta to map Okta user profile to Nuxeo profile.

[![Build Status](https://qa.nuxeo.org/jenkins/buildStatus/icon?job=Sandbox/sandbox_nuxeo-labs-okta-master)](https://qa.nuxeo.org/jenkins/job/Sandbox/job/sandbox_nuxeo-labs-okta-master/)

# Requirements

Build requires the following software:
- git
- maven

# Limitations

The mapping is "fixed"; it assumes the only fields that will be used from Okta are:

* email (also used for the user ID)
* firstName
* lastName
* groups

# Build

```
git clone https://github.com/nuxeo-sandbox/nuxeo-labs-okta
cd nuxeo-labs-okta
mvn clean install
# or 
mvn clean install -DskipTests
```

# Deploy

Install the marketplace package on your Nuxeo instance.

Add a `userResolverClass` parameter to your authenticators contribution in Nuxeo Studio:

```
<parameter name="userResolverClass">nuxeo.labs.okta.core.authentication.OktaUserResolver</parameter>
```

A full Studio contribution example is provided in the "studio" folder. 

# Support

**These features are not part of the Nuxeo Production platform.**

These solutions are provided for inspiration and we encourage customers to use them as code samples and learning resources.

This is a moving project (no API maintenance, no deprecation process, etc.) If any of these solutions are found to be useful for the Nuxeo Platform in general, they will be integrated directly into platform, not maintained here.

# Licensing

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)

# About Nuxeo

Nuxeo dramatically improves how content-based applications are built, managed and deployed, making customers more agile, innovative and successful. Nuxeo provides a next generation, enterprise ready platform for building traditional and cutting-edge content oriented applications. Combining a powerful application development environment with SaaS-based tools and a modular architecture, the Nuxeo Platform and Products provide clear business value to some of the most recognizable brands including Verizon, Electronic Arts, Netflix, Sharp, FICO, the U.S. Navy, and Boeing. Nuxeo is headquartered in New York and Paris.

More information is available at [www.nuxeo.com](http://www.nuxeo.com).

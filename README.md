[<img src="https://sling.apache.org/res/logos/sling.png"/>](https://sling.apache.org)

 [![Build Status](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-org-apache-sling-nosql-couchbase-resourceprovider/job/master/badge/icon)](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-org-apache-sling-nosql-couchbase-resourceprovider/job/master/) [![Test Status](https://img.shields.io/jenkins/tests.svg?jobUrl=https://ci-builds.apache.org/job/Sling/job/modules/job/sling-org-apache-sling-nosql-couchbase-resourceprovider/job/master/)](https://ci-builds.apache.org/job/Sling/job/modules/job/sling-org-apache-sling-nosql-couchbase-resourceprovider/job/master/test/?width=800&height=600) [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=apache_sling-org-apache-sling-nosql-couchbase-resourceprovider&metric=coverage)](https://sonarcloud.io/dashboard?id=apache_sling-org-apache-sling-nosql-couchbase-resourceprovider) [![Sonarcloud Status](https://sonarcloud.io/api/project_badges/measure?project=apache_sling-org-apache-sling-nosql-couchbase-resourceprovider&metric=alert_status)](https://sonarcloud.io/dashboard?id=apache_sling-org-apache-sling-nosql-couchbase-resourceprovider) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.sling/org.apache.sling.nosql.couchbase-resourceprovider/badge.svg)](https://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.apache.sling%22%20a%3A%22org.apache.sling.nosql.couchbase-resourceprovider%22) [![JavaDocs](https://www.javadoc.io/badge/org.apache.sling/org.apache.sling.nosql.couchbase-resourceprovider.svg)](https://www.javadoc.io/doc/org.apache.sling/org.apache.sling.nosql.couchbase-resourceprovider) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![nosql](https://sling.apache.org/badges/group-nosql.svg)](https://github.com/apache/sling-aggregator/blob/master/docs/groups/nosql.md)&#32;[![contrib](https://sling.apache.org/badges/status-contrib.svg)](https://github.com/apache/sling-aggregator/blob/master/docs/status/contrib.md)

# Apache Sling NoSQL Couchbase Resource Provider

This module is part of the [Apache Sling](https://sling.apache.org) project.

Sling ResourceProvider implementation that uses [Couchbase](http://www.couchbase.com/) NoSQL database as persistence.

Based on the "Apache Sling NoSQL Generic Resource Provider" and "Apache Sling NoSQL Couchbase Client".

Couchbase Server 4.0 with N1QL support is required for this implementation.


Configuration on deployment
---------------------------

* To use the resource provider you have to to create a factory configuration for "Apache Sling NoSQL Couchbase Client" with clientId = ´sling-resourceprovider-couchbase´ and propert couchbase host and bucket configuration.
* Additionally a factory configuration for "Apache Sling NoSQL Couchbase Resource Provider Factory" defines the root of the resource tree that should be stored in Couchbase


Run integration tests
---------------------

To run the integration tests you have to set up a real couchbase server and run the tests with this command line (inserting the correct parameters for couchbase host and bucket):

```
mvn -Pcouchbase-integration-test -DcouchbaseHosts=localhost:8091 -DbucketName=test integration-test
```

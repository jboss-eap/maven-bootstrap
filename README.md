A script to bootstrap Maven environment using zip repositories
==============================================================

Usage:

1. Download EAP 6 Maven Repository zip file
2. Download WFK 2 Maven Repository zip file
3. Run `mvn package`

Result:

Your `settings.xml` is generated in upper directory. Reference it from your IDE or from Maven binary

	mvn -s /path/to/generated/settings.xml

Note:
Script will as well create .repository directory, which acts as a local repositary to keep your environment isolated

Troubleshooting
---------------

The script allows you to set path where zip files are stored. Following properties can be used:

* __eap6.enterprise.repository.zip__ - a path to EAP6 Maven Repository zip
* __wfk2.enterprise.repository.zip__ - a path to WFK2 Maven Repository zip
* __eap6.enterprise.repository.dir__ - an absolute path where EAP6 Maven Repository was extracted
* __wfk2.enterprise.repository.dir__ - an absolute path where WFK2 Maven Repository was extracted

On Linux, you can use following Maven command

	mvn clean package -Deap6.enterprise.repository.zip=jboss-eap-6.0.0.DR12-maven-repository.zip \ 
		-Dwfk2.enterprise.repository.zip=jboss-wfk-2.0.0-DR07-repository.zip \
		-Deap6.enterprise.repository.dir=`pwd`/jboss-eap-6.0.0.DR12-maven-repository \ 
		-Dwfk2.enterprise.repository.dir=`pwd`/jboss-wfk-2.0.0-DR07-repository

A script to bootstrap Maven environment using zip repositories
==============================================================

Usage:
1. Download EAP Repository zip file
2. Download WFK Repository zip file
3. Extract both zips
4. Run `mvn package`

Result:

Your `settings.xml` is generated in upper directory. Reference it from your IDE or from Maven binary

Note:
Script will as well create .repository directory, which acts as a local repositary to keep your environment isolated

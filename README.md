# Liferay 6.1.+ SOLR integration web-app #

This project enables Liferay 6.1.+ to use SOLR for content indexing instead of the default indexing engine. It was tested on SOLR 1.4.1, 3.3.0, 4.3.1 versions on both Tomcat (7.0.40) and JBossAS (7.1.1-final) but it could possibly work with much more versions.

At the moment the master branch is aligned with SOLR 4.3.1 branch. If you need SOLR 3.3.0 or 1.4.1 you can switch to the correct branch.

## Usage: ##
* Get SOLR up and running using the schema.xml provided in solr_schema (you can merge your it into your previous schema if you prefer).
* Modify the solr.url property in pom.xml to match your server 
	* for old-style SOLR it's http://host:port/solr
	* for new multi-core style SOLR it's http://host:port/solr/COLLECTION_NAME
* launch "mvn clean package" to compile and generate the web application WAR.
* deploy int your Liferay 6.1.* server using the Liferay HotDeployer
* after successful deployment navigate co Control Panel > Server > Serve Administration and press "Reindex all search indexes."
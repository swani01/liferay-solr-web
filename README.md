# Liferay 6.1+ SOLR integration web-app #

This project enables Liferay 6.1.2 to use SOLR for content indexing instead of internal Lucene. The master branch is aligned with solr 4.3.1 branch.

## Usage: ##
* Get SOLR up and running using the schema.xml provided in solr_schema (you can merge your it into your previous schema if you prefer).
* Modify the solr.url property in pom.xml to match your server 
	* for old-style SOLR it's http://host:port/solr
	* for new multi-core style SOLR it's http://host:port/solr/COLLECTION_NAME
* launch "mvn clean package" to compile and generate the web application WAR.
* deploy int your Liferay 6.1.* server using the Liferay HotDeployer
* after successful deployment navigate co Control Panel > Server > Serve Administration and press "Reindex all search indexes."
Kibana Marvel & Sense with Elastic Search
=========================================

This runs an elasticsearch with kibana for seeing what you have in the thing, you know?
The plugins marvel and sense are installed.

Running
-------

You run this with docker-compose:

    docker-compose up

You will need to update the kibana settings once it has launched:

    curl -XPUT -d '{ "index" : { "max_result_window" : 2147483647 } }' http://localhost:9200/.kibana/_settings

(issue [#5524](https://github.com/elastic/kibana/issues/5524))

You can then view [marvel](http://localhost:5601/app/marvel), [sense](http://localhost:5601/app/sense) or [kibana](http://localhost:5601/app/kibana)

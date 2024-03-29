# elastic-8


1.  LucaWintergerst /observability-example

```https://github.com/LucaWintergerst/observability-example```

```
ElasticCC: Getting Started With Elastic APM
   
   https://www.youtube.com/watch?v=jRSGj65YLA8
```



2. Henrique mauri

```https://www.youtube.com/watch?v=Rb-3tZq759Q```

```https://github.com/hgmauri```

```https://henriquemauri.net/```


## DOCUMENTAÇÕES

> https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping-date-format.html

> https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping-params.html


## GROK DEBUG

* https://grokdebug.herokuapp.com/

* https://grokdebugger.com/

* https://regex101.com/

## LOGSTASH PATTERNS

* https://github.com/hpcugent/logstash-patterns/blob/master/files/grok-patterns

* https://discuss.elastic.co/t/what-is-greedydata/122078

* https://grokdebugger.com/patterns/grok-patterns.txt

* https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.0/html/configuration_guide/logging_with_jboss_eap

## DOCUMENTACOES

* https://frednotes.wordpress.com/2021/08/25/wildfly-elastic/

> Using Grok with Elasticsearch to add structure to your data

* https://alexmarquardt.com/using-grok-with-elasticsearch-to-add-structure-to-your-data/

> Common Logstash Use cases with GROK, JSON and Mutate filters.
* https://itnext.io/common-logstash-use-cases-with-grok-json-and-mutate-filters-elk-logstash-in-docker-filebeat-871ed58c7651


## GROK PATTERNES

http://localhost:5601/app/dev_tools#/grokdebugger

``` Grok Pattern

2001-12-29 03:02:19,305 ERROR [stderr] (default task-345678) Caused by: br.com.microsoft.jape.PersistenceException: Make Your Choice.

(?:%{TIMESTAMP_ISO8601:data}) (?:%{LOGLEVEL:level}) \[(%{WORD:method})\] \(%{WORD:method2)\) (?<message>.*)$

```

```

(?:%{TIMESTAMP_ISO8601:data}) (?:%{LOGLEVEL:level}) \[(%{WORD:method})\] \(%{WORD:method2)\) (?<message>.*)$

```

```
2002-12-29 03:02:19,305 ERROR [stderr] (default task-7277) Caused by: com.apple.jape.PersistenceException: Projeto já concluído.

(?<TIMESTAMP_ISO8601>\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2},\d{3}) (?<level>[^ ]*)\s+\[(?<method>.*?)\] \((?<thread>.*?)\) (?<message>.*)$
```

```
2002-01-29 11:33:21,565 INFO  [stdout] (com.microsoft.modelcore [ SEUL INTERNAL PROCESSOR ]) Script recuperacao SEUL 'sql/enviar-email-tambau.sql': 0 linhas.

(?:%{TIMESTAMP_ISO8601:data}) (?:%{LOGLEVEL:level})\s+\[(?<method>.*?)\] \((?<thread>.*?)\) (?<message>.*)$

```

```
2002-12-29 10:59:21,565 INFO  [stdout] (com.microsoft.modelcore [ INTERNAL TAMBAU ]) Script recuperacao DJTOTO 'sql/fazer-pizza-passos.sql': 7 linhas.

(?:%{TIMESTAMP_ISO8601:data}) (?:%{LOGLEVEL:level})\s+\[(?<method>.*?)\] \((%{DATA:thread})\) (%{DATA:msg})$

```

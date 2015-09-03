# Axibase Time Series Database plugin for Grafana

## Installation guide

Copy ```atsd/``` into ```<grafana-2.x.x source directory>/public/app/plugins/datasource/``` directory, then proceed as you would normally do with any built-in plugin.

## Query editor overview

![Overall](https://axibase.com/wp-content/uploads/2015/09/17-overall.png)

* Clicking the 'Submit' button results in a 'get_data' request. The 'Cache' button is for dropping the meta-data cache (described below).
![Default](https://axibase.com/wp-content/uploads/2015/09/00-default.png)

* Disconnect interval option makes use of Grafana's null point mode. If there is a gap in data bigger than the indicated value, a couple of nulls are inserted on each side of the gap.
![Disconnect](https://axibase.com/wp-content/uploads/2015/09/01-disconnect.png)

* There is auto-complete in the entity field. This and other meta-data request results, such as metric lists and tag combinations, are cached for 5 minutes, and you can drop the cache with the 'Cache' button.
![Entity](https://axibase.com/wp-content/uploads/2015/09/02-entity.png)

* The same works for the metric field.
![Metric](https://axibase.com/wp-content/uploads/2015/09/03-metric.png)

* For the long point-separated metric names there is a token mode like the one in Graphite data source.
![Metric mode](https://axibase.com/wp-content/uploads/2015/09/04-metric_mode.png)

* '+' to add a new token, 'X' to delete the last one, 'tick' to finish.
![Segment 1](https://axibase.com/wp-content/uploads/2015/09/05-segment_1.png)
![Segment 2](https://axibase.com/wp-content/uploads/2015/09/06-segment_2.png)
![Segment 3](https://axibase.com/wp-content/uploads/2015/09/07-segment_3.png)

* This is what it looks like in the end.
![As tokens](https://axibase.com/wp-content/uploads/2015/09/08-as_tokens.png)

* You can switch between modes by clicking 'as tokens' / 'as text'.
![As text](https://axibase.com/wp-content/uploads/2015/09/09-as_text.png)

* The queries support all ATSD statistic aggregators.
![Aggregator](https://axibase.com/wp-content/uploads/2015/09/10-aggregator.png)

* You can denote the aggregation period.
![Period](https://axibase.com/wp-content/uploads/2015/09/11-period.png)

* There are two tag editing modes. The first one is 'Tag editor', where you add tag name-value pairs one by one with the help of auto-complete.
![Tag name](https://axibase.com/wp-content/uploads/2015/09/12-tag_name.png)

* Auto-complete shows only the possible values, taking into account all the previous tags.
![Tag value](https://axibase.com/wp-content/uploads/2015/09/13-tag_value.png)

* '+' to add a new name-value pair, 'X' to delete the last one. You can use ATSD regular expressions to match more than one tag value.
![Tag editor](https://axibase.com/wp-content/uploads/2015/09/14-tag_editor.png)

* Tag selector, on the other hand, shows all the possible tag combinations and allows to pick the ones you want to plot on a graph.
![Tag selector](https://axibase.com/wp-content/uploads/2015/09/15-tag_selector.png)

* After clicking the 'Submit' button the graph appears.
![Result](https://axibase.com/wp-content/uploads/2015/09/16-result.png)
# metrics-module-tweets
This Social Network Metric defines the searching of specific Keyword into the Twitter Community to measure the spreading of this topic.


## Specification

1. **Resource**: Twitter Streaming API
2. **Source**:  Twitter Community, streams of the public data flowing through Twitter.
3. **Metric parameters**:
  1. **Query**: keyword or comma-separated words delivered on the stream.
  2. **Scope**: Includes all words. This will be over-inclusive.
  3. **Output**: Number of public tweets.

4. **Library description**: 
  1. **hits.js**: return the list and count of different tweets languages where it has been found the query (in the public data flowing through Twitter):
  2. **Hits(conf)**: setup the secure authorized requests to access the Twitter API
  3. **conf**:  data structure or file with details of OAuth data (consumer_key, consumer_secret, access_token, access_token_secret).
  4. **Hits.get(params, timescan, callback)**:
    - **params**: Keyword or keywords are specified by a comma-separated list.
    - **timescan**: Time in seconds to scan the Streams of the public data flowing through Twitter.
    - **callback**: function (results),  data is the parsed data.
  5. **twitter.js**: Twitter API Client for nodeJS.


## Example:
1. **Input**: Uniprot
2. **Query**: https://stream.twitter.com/1.1/statuses/filter.json?track=Uniprot
3. **Output**: Total tweets: 29

> Information about Twitter stream API: https://dev.twitter.com/streaming/overview/request-parameters#track

> Secure Authorized Requests: 
Twitter uses OAuth to provide authorized access to its API. It is possible get your consumer key and secret key, registering your application following this guide: https://dev.twitter.com/oauth/overview/application-owner-access-tokens.

## Git

`https://github.com/BioPisCO/metrics-module-tweets.git`

## Requirements

  1. Nodejs
  2. npm

## Install library dependencies
  
  `nmp install`

## Install library dependencies

  `node example/example-twit.js Uniprot`

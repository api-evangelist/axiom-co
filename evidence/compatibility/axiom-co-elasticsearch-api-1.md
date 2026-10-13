<!-- fetched 2026-10-13 from https://axiom.co/docs/send-data/elasticsearch-bulk-api by sweep-shape-compat.py; text extracted from the provider's own page -->

Send data from Elastic Bulk API to Axiom | Axiom Docs 
 Docs Documentation Query Reference API Reference What are you looking for? Search Open Console → → 
 Documentation Query Reference API Reference Platform overview
 What is Axiom? Quickstart Architecture Features Fundamentals Datasets 
 Edge deployments 
 Limits 
 Performance 
 Optimize usage 
 Requirements 
 Semantic conventions 
 Glossary 
 Tour 
 Security Roadmap 
 Send data
 Reference architectures Methods 
 Understand data
 Console Query Builder 
 Editor 
 Query results 
 Visualize 
 Traces 
 Metrics 
 Correlations 
 Save queries 
 Stream 
 Dashboard Create 
 Elements Create 
 Configure 
 Element types Gauge 
 Heatmap 
 Log stream 
 Monitor list 
 Note 
 Pie chart 
 Scatter plot 
 Statistic 
 Table 
 Time series 
 Sections 
 Configure 
 Filter 
 Annotate 
 Monitor Overview 
 View status 
 Configure 
 Examples 
 Monitor types Anomaly 
 Match 
 Threshold 
 Alerting Overview 
 Configure 
 Notifier types Custom Webhook 
 Discord 
 Email 
 Microsoft Teams 
 Opsgenie 
 PagerDuty 
 Slack 
 Manage Datasets Overview 
 Views 
 Virtual fields 
 Access RBAC 
 Tokens 
 CLI 
 Organization Audit log 
 Settings 
 Usage and billing 
 Profile 
 Extend Overview 
 AWS Lambda 
 AWS PrivateLink 
 Cloudflare Workers 
 Cloudflare Logpush 
 Convex 
 Grafana 
 Hex 
 Netlify 
 Supabase 
 Tailscale 
 Terraform 
 Unkey 
 Vercel 
 Intelligence Overview 
 Spotlight 
 AI agents Overview 
 MCP Server Overview 
 Tools 
 Query cost limits 
 Agent-created orgs 
 Skills Overview 
 Axiom alerting 
 Build dashboards 
 Control costs 
 SRE 
 Translate SPL to APL 
 Splunk Overview 
 Splunk app Install and configure 
 Commands 
 Examples 
 Portal How it works 
 Set up standard mode 
 Set up transparent mode 
 Observability Cloud 
 OCSF data 
 OCSF as CIM 
 SPL command support 
 Examples 
 Monitor and troubleshoot 
 Use cases
 Observability Product analytics OCSF security data Overview 
 Send data 
 Query data 
 LLM observability Overview 
 Use Axiom AI SDK 
 Manual instrumentation 
 GenAI attributes 
 Redaction policies 
 Miscellaneous
 LLMs Overview 
 List of docs pages 
 Full docs 
 Query reference 
 FAQs Legal Acceptable use policy 
 Axiom for Startups terms 
 Cookies 
 Data processing 
 HIPAA 
 Partner agreement 
 Partner program guide 
 Privacy policy 
 SLA 
 Terms of service 
 Terms of use 
 Copy page Copied 
 Send data from Elastic Bulk API to Axiom
 This page explains how to get started with migrating from Elasticsearch to Axiom using the Elastic Bulk API
 Axiom is a log management platform that offers an Elasticsearch Bulk API emulation to facilitate migration from Elasticsearch or integration with tools that support the Elasticsearch Bulk API.
 Using the Elastic Bulk API and Axiom in your app provides a robust way to store and manage logs.
 The Elasticsearch Bulk API expects the timestamp to be formatted as @timestamp , not _time . For example:
 JSON 
 { " index " : { " _index " : "myindex" , " _id " : "1" }} { " @timestamp " : "2024-01-07T12:00:00Z" , " message " : "axiom elastic bulk" , " severity " : "INFO" } 
 Prerequisites 
 Create an Axiom account .
 Create a dataset in Axiom where you send your data.
 Create an API token in Axiom with permissions to ingest data to the dataset you have created.
 Send logs to Axiom using the Elasticsearch Bulk API and Go 
 To send logs to Axiom using the Elasticsearch Bulk API and Go, use the net/http package to create and send the HTTP request.
 Prepare your data 
 The data needs to be formatted as per the Bulk API’s requirements. Here’s a simple example of how to prepare your data:
 JSON 
 data := { " index " : { " _index " : "myindex" , " _id " : "1" }} { " @timestamp " : "2023-06-06T12:00:00Z" , " message " : "axiom elastic bulk" , " severity " : "INFO" } { " index " : { " _index " : "myindex" , " _id " : "2" }} { " @timestamp " : "2023-06-06T12:00:01Z" , " message " : "axiom elastic bulk api" , " severity " : "ERROR" } 
 Send data to Axiom 
 Get an Axiom API token for the Authorization header, and create a dataset .
 go 
 package main import ( "bytes" "fmt" "io/ioutil" "log" "net/http" ) func main () { data := [] byte ( `{"index": {"_index": "myindex", "_id": "1"}} {"@timestamp": "2023-06-06T12:00:00Z", "message": "axiom elastic bulk", "severity": "INFO"} {"index": {"_index": "myindex", "_id": "2"}} {"@timestamp": "2023-06-06T12:00:01Z", "message": "axiom elastic bulk api", "severity": "ERROR"} ` ) // Create a new request using http req , err := http . NewRequest ( "POST" , "https://AXIOM_DOMAIN:443/v1/ingest/DATASET_NAME/elastic/_bulk" , bytes . NewBuffer ( data )) if err != nil { log . Fatalf ( "Error creating request: %v " , err ) } // Add authorization header to the request req . Header . Add ( "Authorization" , "Bearer API_TOKEN" ) req . Header . Add ( "Content-Type" , "application/x-ndjson" ) // Send request using http.Client client := & http . Client {} resp , err := client . Do ( req ) if err != nil { log . Fatalf ( "Error on response: %v " , err ) } defer resp . Body . Close () // Read and print the response body body , err := ioutil . ReadAll ( resp . Body ) if err != nil { log . Fatalf ( "Error reading response body: %v " , err ) } fmt . Printf ( "Response status: %s\n Response body: %s\n " , resp . Status , string ( body )) } 
 Info 
 Replace AXIOM_DOMAIN with the base domain of your edge deployment. For more information, see Edge deployments .
 Replace API_TOKEN with the Axiom API token you have generated. For added security, store the API token in an environment variable.
 Replace DATASET_NAME with the name of the Axiom dataset where you send your data.
 Send logs to Axiom using the Elasticsearch Bulk API and Python 
 To send logs to Axiom using the Elasticsearch Bulk API and Python, use the built-in requests library.
 Prepare your data 
 The data sent needs to be formatted as per the Bulk API’s requirements. Here’s a simple example of how to prepare the data:
 JSON 
 data = """ {" index ": {" _index ": " myindex ", " _id ": " 1 "}} {" @timestamp ": " 2023-06-06 T 12 : 00 : 00 Z ", " message ": " Log message 1 ", " severity ": " INFO "} {" index ": {" _index ": " myindex ", " _id ": " 2 "}} {" @timestamp ": " 2023-06-06 T 12 : 00 : 01 Z ", " message ": " Log message 2 ", " severity ": " ERROR "} """ 
 Send data to Axiom 
 Obtain an Axiom API token for the Authorization header, and dataset .
 python 
 import requests import json data = """ {"index": {"_index": "myindex", "_id": "1"}} {"@timestamp": "2024-01-07T12:00:00Z", "message": "axiom elastic bulk", "severity": "INFO"} {"index": {"_index": "myindex", "_id": "2"}} {"@timestamp": "2024-01-07T12:00:01Z", "message": "Log message 2", "severity": "ERROR"} """ # Replace these with your actual dataset name and API token dataset = "DATASET_NAME" api_token = "API_TOKEN" # The URL for the bulk API url = f 'https://AXIOM_DOMAIN:443/v1/ingest/ { dataset } /elastic/_bulk' try : response = requests . post ( url , data = data , headers ={ 'Content-Type' : 'application/x-ndjson' , 'Authorization' : f 'Bearer { api_token } ' } ) response . raise_for_status () except requests . HTTPError as http_err : print ( f 'HTTP error occurred: { http_err } ' ) print ( 'Response:' , response . text ) except Exception as err : print ( f 'Other error occurred: { err } ' ) else : print ( 'Success!' ) try : print ( response . json ()) except json . JSONDecodeError : print ( response . text ) 
 Info 
 Replace AXIOM_DOMAIN with the base domain of your edge deployment. For more information, see Edge deployments .
 Replace API_TOKEN with the Axiom API token you have generated. For added security, store the API token in an environment variable.
 Replace DATASET_NAME with the name of the Axiom dataset where you send your data.
 Send logs to Axiom using the Elasticsearch Bulk API and JavaScript 
 Use the axios library in JavaScript to send logs to Axiom using the Elasticsearch Bulk API.
 Prepare your data 
 The data sent needs to be formatted as per the Bulk API’s requirements. Here’s a simple example of how to prepare the data:
 JSON 
 let data = ` { " index " : { " _index " : "myindex" , " _id " : "1" }} { " @timestamp " : "2023-06-06T12:00:00Z" , " message " : "Log message 1" , " severity " : "INFO" } { " index " : { " _index " : "myindex" , " _id " : "2" }} { " @timestamp " : "2023-06-06T12:00:01Z" , " message " : "Log message 2" , " severity " : "ERROR" } `; 
 Send data to Axiom 
 Obtain an Axiom API token for the Authorization header, and dataset .
 javascript 
 const axios = require ( 'axios' ); // Axiom elastic API URL const AxiomApiUrl = ' https :// AXIOM_DOMAIN : 443 / v1 / ingest / DATASET_NAME / elastic / _bulk ' ; // Your Axiom API token const AxiomToken = ' API_TOKEN ' ; // The logs data retrieved from Elasticsearch const logs = [ { "index" : { "_index" : "myindex" , "_id" : "1" }}, { "@timestamp" : "2023-06-06T12:00:00Z" , "message" : "axiom logging" , "severity" : "INFO" }, { "index" : { "_index" : "myindex" , "_id" : "2" }}, { "@timestamp" : "2023-06-06T12:00:01Z" , "message" : "axiom log data" , "severity" : "ERROR" } ] ; // Convert the logs to a single string with newline separators const data = logs . map ( log => JSON . stringify ( log )). join ( ' \n ' ) + ' \n ' ; axios . post ( AxiomApiUrl , data , { headers : { 'Content-Type' : 'application/x-ndjson' , 'Authorization' : `Bearer ${ AxiomToken } ` } }) . then (( response ) => { console . log ( 'Response Status:' , response . status ); console . log ( 'Response Data:' , response . data ); }) . catch (( error ) => { console . error ( 'Error:' , error . response ? error . response . data : error . message ); }); 
 Info 
 Replace AXIOM_DOMAIN with the base domain of your edge deployment. For more information, see Edge deployments .
 Replace API_TOKEN with the Axiom API token you have generated. For added security, store the API token in an environment variable.
 Replace DATASET_NAME with the name of the Axiom dataset where you send your data.
 Send logs to Axiom using the Elasticsearch Bulk API and PHP 
 To send logs from PHP to Axiom using the Elasticsearch Bulk API, make sure you have installed the necessary PHP libraries: Guzzle for making HTTP requests and JsonMachine for handling newline-delimited JSON data.
 Prepare your data 
 The data sent needs to be formatted as per the Bulk API’s requirements. Here’s a simple example of how to prepare the data:
 JSON 
 $data = <<<EOD { " index " : { " _index " : "myindex" , " _id " : "1" }} { " @timestamp " : "2023-06-06T12:00:00Z" , " message " : "Log message 1" , " severity " : "INFO" } { " index " : { " _index " : "myindex" , " _id " : "2" }} { " @timestamp " : "2023-06-06T12:00:01Z" , " message " : "Log message 2" , " severity " : "ERROR" } EOD; 
 Send data to Axiom 
 php 
 <? php require 'vendor/autoload.php' ; use GuzzleHttp \ Client ; $ client = new Client ([ 'base_uri' => 'https://AXIOM_DOMAIN:443/v1/ingest/DATASET_NAME/elastic/_bulk' , // Update with your Axiom host 'timeout' => 2 . 0 , ]); // Your Axiom API token $ AxiomToken = 'API_TOKEN' ; // The logs data retrieved from Elasticsearch // Note: Replace this with your actual code to retrieve logs from Elasticsearch $ logs = [ [ "@timestamp" => "2023-06-06T12:00:00Z" , "message" => "axiom logger" , "severity" => "INFO" ], [ "@timestamp" => "2023-06-06T12:00:01Z" , "message" => "axiom logging elasticsearch" , "severity" => "ERROR" ] ]; $ events = array_map ( function ($ log ) { return [ '@timestamp' => $ log [ '@timestamp' ], 'attributes' => $ log ]; }, $ logs ); // Create the payload for Axiom $ payload = [ 'tags' => [ 'source' => 'myapplication' , 'host' => 'myhost' ], 'events' => $ events ]; try { $ response = $ client -> post ( '' , [ 'headers' => [ 'Authorization' => 'Bearer ' . $ AxiomToken , 'Content-Type' => 'application/x-ndjson' , ], 'json' => $ payload , ]); // handle response here $ statusCode = $ response -> getStatusCode (); $ content = $ response -> getBody (); echo "Status code: $ statusCode \n Content: $ content " ; } catch (\ Exception $ e ) { // handle exception here echo "Error: " . $ e -> getMessage (); } 
 Info 
 Replace AXIOM_DOMAIN with the base domain of your edge deployment. For more information, see Edge deployments .
 Replace API_TOKEN with the Axiom API token you have generated. For added security, store the API token in an environment variable.
 Replace DATASET_NAME with the name of the Axiom dataset where you send your data.
 Was this page helpful? Yes No 
 Suggest edits on GitHub 
 On this page 
 Send logs to Axiom using the Elasticsearch Bulk API and Go Prepare your data Send data to Axiom Send logs to Axiom using the Elasticsearch Bulk API and Python Prepare your data Send data to Axiom Send logs to Axiom using the Elasticsearch Bulk API and JavaScript Prepare your data Send data to Axiom Send logs to Axiom using the Elasticsearch Bulk API and PHP Prepare your data Send data to Axiom 
 Ask AI ⌘ I

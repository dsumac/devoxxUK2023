# Scaling: from 0 to 20 million

From on-premise to cloud and go back at sofascore

## Context

- sport application: native, web etc.
- high traffic

## way to evolving

- 1 server with backup on the same machine 😊
- memory using
  - cache using: memcache
- apache httpd + php
- varnish using
  - request coalescing (merge requests)
- from ?? to mongoDb to postgresql to  

### mongoDB using

- why ? because ! => not ADR !
- drawbacks
  - replication issues
  - data types errors (no support for foreign keys)
  - difficult to analyse data

- go back to postgresql

### move cache layer

- outside of the cloud
  - reduced * 10 of the cost

### longer cache

- from 10s to 1 mins

### what's happens if nb users exceed users capacity 

- dedicated + VPS
  - scalling

### experience is different in the world
- put varnish all around the world
  - distributed cache

### datacenter burned (on premise)
- ovh

### kubernetes using
- it was difficult

### real time updates
- NATS messaging

## Conclusion

- Infrasctructure represents 0.8 % of revenue
- be stateless where possible
- know how users interct with the app
- cache !
- the right tool for the job and chage if necessary
- optimize what you have need
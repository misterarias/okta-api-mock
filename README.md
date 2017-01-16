Okta mock server
===============

A dockerized mocked Okta API server, forked from Joel Franusic's awesome work: https://github.com/jpf/okta-api-mock
**WARNING** This is a service that Joel Franusic wrote for himself, so it will have lots of rough edges.

To run, you can use the usual docker build/run flow, or add it to your composer of choice.

Environment variables that are used to modify the server:
* FLASK_PORT (defaults to 5000)
* FLASK_DEBUG (defaults to `False`)

Run example
```
docker build -t mock-server mock-server/

# This would also mount the app for live development
docker run --rm -p 5000:5000 -e FLASK_DEBUG=True -v mock-server:/site   -t mock-server
```

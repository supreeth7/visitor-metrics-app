# Visitor Metrics Operator
The Visitors Site tracks information about each request to its home page. Each time the page is refreshed, an entry is stored with details about the client, backend server,
and timestamp. The home page displays a list of the most recent visits.

## How to

1. Create a new project.
2. Create a generic secret with string literals `username` `password`.
3. Clone the repo, cd into it and run the command `oc create -f .` This will create all the required deployments and services.
4. Check if pods have been created and are running without any errors `oc get pods`.
5. Create a route for external access, `oc expose svc <SVC_NAME> --hostname=<YOUR_HOSTNAME>`
6. Run `oc get routes` and navigate to exposed host through the browser.

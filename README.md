# Hubot Jira

A hubot script to list jira issues, statuses and move issues.

Commands it knows:

* hubot move jira \<issue ID> to \<status> - Changes the status of \<issue ID> to \<status>
* hubot jira status - List the available statuses
* hubot jira projects - list known project keys (at time hubot started)
* hubot jira create \<projectKey> \<taskType> subject line: description

The `create` command requires that the `$JIRA_USERNAME` user has the *Modify
Reporter* permission. This can be individually assigned in the permission
scheme to this user. With this permission, the issues are created using the ID
of the person issuing the request. This has been tested using the Slack
connector. The assumption is that the usernames in Jira match the usernames
from Slack.

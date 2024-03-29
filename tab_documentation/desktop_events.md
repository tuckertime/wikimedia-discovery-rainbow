Desktop search
=======

User actions that we track around search on the desktop website generally fall into three categories:

1. The start of a user's search session;
2. The presentation of the user with a results page, and;
3. A user clicking through to an article in the results page.

These three things are tracked via the [EventLogging 'search' schema](https://meta.wikimedia.org/wiki/Schema:Search), and stored to
a database. The results are then aggregated and anonymised, and presented on this page. For performance/privacy reasons we randomly sample what we store, so the actual numbers are a vast understatement of how many user actions our servers receive - what's more interesting is how they change over time. In the case of desktop search, this sampling rate is **0.1%**.

Outages and inaccuracies
------
There are occasionally going to be outages that will affect the accuracy of data. To make it easier to rely on the data (or not!) they are listed here, from most- to least-recent.

* Between 2 October 2015 and 28 October 2015 we were not logging any events from the Search schema. There was a change in core that broke the code being inserted into pages. Those pages were cached into varnish so an alternate solution had to be taken. that was delayed because of deployment freezes. The change in core only broke it because the way the code was added from our side was technically wrong, but happened to work anyways.
* Between 5 May and 6 May 2015, approximately 40% of incoming EventLogging data was lost due to a wider EventLogging outage. You can read more about the outage [here](https://wikitech.wikimedia.org/wiki/Incident_documentation/20150506-EventLogging).
* Data in late September/early October 2015 is unavailable due to another bug in EventLogging as a whole, which impacted data collection.

Questions, bug reports, and feature suggestions
------
For technical, non-bug questions, [email Mikhail](mailto:mpopov@wikimedia.org?subject=Dashboard%20Question). If you experience a bug or notice something wrong or have a suggestion, [open a ticket in Phabricator](https://phabricator.wikimedia.org/maniphest/task/create/?projects=Discovery) in the Discovery board or [email Dan](mailto:dgarry@wikimedia.org?subject=Dashboard%20Question).

<hr style="border-color: gray;">
<p style="font-size: small; color: gray;">
  <strong>Link to this dashboard:</strong>
  <a href="http://discovery.wmflabs.org/metrics/#desktop_events">
    http://discovery.wmflabs.org/metrics/#desktop_events
  </a>
</p>

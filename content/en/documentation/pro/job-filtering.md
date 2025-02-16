---
title: "Job Filtering"
subtitle: "JobRunr Pro Dashboard - the backoffice to your code"
date: 2020-08-27T11:12:23+02:00
layout: "documentation"
menu: 
  main: 
    identifier: job-filtering
    parent: 'jobrunr-pro'
    weight: 3
---
Are you processing millions of jobs? Do you need to find that one job and find out if it succeeded? JobRunr Pro has you covered - thanks to a new feature called Job Filtering.

<figure>
<img src="/documentation/job-filters.gif" class="kg-image">
<figcaption>Thanks to job filters, you can quickly find the job you are interested in.</figcaption>
</figure>

> Note that users using __Redis__ as StorageProvider can only filter on State, Job Signature, Queue and ServerTag.

You can combine multiple filters to quickly find the job you are looking for like:
- Job Name
- Job Signature / Method Signature
- Job Fingerprint / Complete method with serialized parameters (toString())
- The queue the job was submitted on
- The server tag of the job
- Created after / Created before
- Updated after / Updated before 

To see a complete demo of JobRunr Pro with job filtering, have a look at this [blog post]({{< ref "/blog/2021-07-12-jobrunr-pro-v3.4.0.md" >}}).

> This feature works great in combination with the [custom delete policies]({{< ref "custom-delete-policy.md" >}}). As you keep less data in your storage provider (either SQL or NoSQL), job filtering will be faster if there is less data.
---
tags:
  - Personal-Blog
---

*Start time:* 23:21

**Story:** 
As the site owner, I want to be able to schedule blog posts
So that I can write a batch of posts as and when I like and schedule when the posts publish

**Acceptance Criteria (as appropriate):**
- Finish setting up scheduler.

**Comments:** 
At the moment we are testing in a table called `scheduled_posts` and we want to, on a cron job every minute check for if a post can be published. If so, it needs to push to the `staging_published` table. There are endpoints for `posts` (`/`), `scheduled_posts` (`/scheduled-posts`) and `staging_published` (`/staging_published`).

Once done, I need to then swap away from `staging_published` to `posts`. I can then, in future, setup a feature flag to swap to `staging_published` whenever I want to test new postgres functionality.

I may need to understand why powershell isn't accepting postgresql installations.

NOTE: The functionality exists now. I use DBeaver to manipulate the postgres server. I just need to create a cron job to run the functionality... Schedules for Heroku seems to be a free way to go about this.

*Finish time:* 
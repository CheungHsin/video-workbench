# Video Workbench / Timeline Agent

Experimental agent that manages video projects with persistent state in Postgres.

## Core Architecture
- Prisma + PostgreSQL (Project → Script/Scene → Asset → TimelineTrack + Keyframe)
- Long-running agent loop that treats the DB as source of truth
- Selective state hydration + transactional updates
- Error recovery with max retries → needs_human
- Slack as primary human interface
- Delegates heavy coding tasks to short-lived Devin sessions

v1 in progress.

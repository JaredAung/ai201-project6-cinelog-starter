# PR Response Doc — CineLog Watchlist Feature

## AI Usage
<!-- Fill in at the end — how you used AI tools during this project -->

## Comment 1 — Rename
**What I did:** 
Asked Claude to rename save_to_watchlist() to add_to_watchlist() and update where the function is called also. 
**How I verified:**
grep -rn "save_to_watchlist" => to ensure that the old functiin name doesn't exist anywhere in the codebase

## Comment 2 — Deduplication
**What I did:** 
Checked how the deduplication is handled in add_to_collection() in services/collection_service.py. Copy the exact same logic for add_to_watchlist()
**How I verified:**
Verified by checking how close the implementation is to deduplication logic in add_to_collection(). 

## Comment 3 — Missing test
**What I did:**
Checked test_add_to_collection_nonexistent_film_raises and how the test operates. 
**How I verified:**
Ran pytest tests/test_watchlist.py -v and the test passed. 

## Comment 4 — Default visibility
**My position:**
**Reasoning:**
**Tradeoff acknowledged:**

## Comment 5 — Sort order
**My position:**
**Reasoning:**
**Engagement with reviewer's point:**

## Comment 6 — Rebase
**What conflicted:**
**How I resolved it:**
**How I verified no conflict remains:**

## PR Description
<!-- Written at the end — feature overview, design decisions, manual testing steps -->
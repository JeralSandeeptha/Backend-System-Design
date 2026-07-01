# Write Around

- Directly write to the DB
- Do not update the cache
- Invalidate the cache

---

![Image](../../images/write-around.png)

---

## Pros

- Good approach for Heavy Read application

- Resolves Inconsistency problem between Cache and DB

## Cons

- For new data read, there will always be CACHE-MISS first. (to resolve this, generally we can pre-heat the cache)

- If DB is down, Write operation will fail

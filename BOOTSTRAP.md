# Bootstrap

## Standard invocation

```text
@SSalMuk-Plugin personal-learning-lab <subject> 이어서 공부하자
```

## Startup procedure

1. enter `/shared/personal-learning-lab`
2. `git pull --ff-only` when a remote is configured
3. read `SYSTEM.md`
4. read `learner/LEARNER.md`
5. resolve the requested subject directory
6. read its `STATE.json`
7. read the latest relevant session summary
8. load only the common and subject skills required for the current task
9. continue from the learner's current state instead of restarting from zero

## Shutdown procedure

After a meaningful learning session:

1. update subject state
2. create or update the session summary
3. apply justified learner/skill improvements
4. validate JSON files
5. review `git diff`
6. commit
7. push

Do not create a commit when nothing persistent changed.

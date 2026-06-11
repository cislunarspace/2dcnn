# Issue tracker

Issues live in **GitHub Issues** for `cislunarspace/2dcnn`.

## Creating issues

Use the `gh` CLI:

```bash
gh issue create --title "<title>" --body "<description>"
```

Optionally add labels, assignees, or a milestone:

```bash
gh issue create --title "<title>" --body "<body>" --label "needs-triage" --assignee @me
```

## Reading issues

```bash
gh issue list                          # open issues
gh issue view <number>                 # single issue
gh issue list --label "needs-triage"   # by label
```

## Commenting

```bash
gh issue comment <number> --body "<comment>"
```

## Closing

```bash
gh issue close <number>
```

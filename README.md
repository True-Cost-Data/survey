# TrueCost Surveys

Hugo site hosting [Formbricks](https://formbricks.com) surveys for the [TrueCost](https://github.com/alx/true_cost) project.

**Live**: https://true-cost-data.github.io/survey

## Surveys

| Survey | Audience | Status |
|--------|----------|--------|
| [Customer Discovery](/customer-discovery/) | Operations / Procurement leads | Active |
| [Pilot Onboarding](/pilot-onboarding/) | Pilot participants | Active |
| [CEO Dashboard Feedback](/role-ceo/) | CEO / Founder | Active |
| [CFO Dashboard Feedback](/role-cfo/) | CFO / Finance lead | Active |
| [Phase 2 Feature Vote](/feature-vote/) | All TrueCost users | Active |

## Adding a survey

1. Create a Formbricks survey at [app.formbricks.com](https://app.formbricks.com)
2. Copy the survey ID from the share URL: `https://app.formbricks.com/s/<SURVEY_ID>`
3. Set `formbricks_survey_id: "<SURVEY_ID>"` in the corresponding `content/*.md` file
4. Commit — GitHub Actions deploys automatically

## Adding a new survey page

```bash
# Create content file
cat > content/my-new-survey.md << 'EOF'
---
title: "My New Survey"
type: surveys
icon: "📋"
description: "Survey description here."
status: active
audience: "Target audience"
duration: "5 min"
formbricks_survey_id: ""
weight: 6
---
EOF
```

Then add it to the menu in `hugo.yaml`.

## Local development

```bash
hugo server
# → http://localhost:1313/survey/
```

## Deploy

Automatic on push to `main`. Manual: Actions → Deploy to GitHub Pages → Run workflow.

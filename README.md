# test_github_actions
This repository for testing github actions

## RUN event "webhook-one"
curl -H "Authorization: token <GITHUB_TOKEN>" \
    --request POST \
    --data '{"event_type": "webhook-one", "client_payload": {"version": "20.30" }}' \
    https://api.github.com/repos/Varagon007/test_github_actions/dispatches

## GET workflow status
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: token <GITHUB_TOKEN>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/Varagon007/test_github_actions/actions/runs
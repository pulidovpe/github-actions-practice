# github-actions-practice
Github Action Practice

Testing CI on Multi-Events

## Manual Events

gh workflow run .github/workflows/manual.yaml \
-f name=mona \                            
-f greeting=hello \
-F data=@more-files/encoded_file.txt

## Webhook Events
curl -X POST \
-H "Accept: application/vnd.github+json" \
-H "Authorization: token ${TOKEN}" \
-d '{"event_type": "webhook", "client_payload": {"key": "value"} }' \
https://api.github.com/repos/pulidovpe/github-actions-practice/dispatches
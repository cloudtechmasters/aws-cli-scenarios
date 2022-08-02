# aws-cli-scenarios
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql <br />
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' <br />
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.' <br />
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.username' <br />
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.password'

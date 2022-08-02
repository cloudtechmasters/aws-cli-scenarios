# aws-cli-scenarios
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString'
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.'
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.username'
aws secretsmanager get-secret-value --secret-id prod/App1/Mysql | jq '.SecretString' | sed -e 's/\\//g' -e 's/^"//g' -e 's/"$//g' |jq '.password'

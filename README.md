# Usage

Use this docker to schedule jobs with JSON calls. jq binary is added to parse result:

```sh
docker run --rm --name curl gintsgints/jq_curl:latest /bin/sh -c 'export TOKEN=`curl -H "Content-Type: application/json" --request POST -d "{\"username\":\"apiuser\",\"password\":\"apipassword\"}" http://10.91.57.165:3001/api/auth/local | jq -r ".token"`
curl -H "Content-Type: application/json" --request GET http://10.91.57.165:3001/api/vk"
```

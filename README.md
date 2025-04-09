latest time zone : https://data.iana.org/time-zones/releases/

```bash
date +%Y
year=$(date +%Y)
curl https://data.iana.org/time-zones/releases/tzdata$((year + 1))a.tar.gz

if [ $? -eq 0 ];
  wget https://data.iana.org/time-zones/releases/tzdata$((year + 1))a.tar.gz
else
  echo  "time zone is up to dated" 
fi
```

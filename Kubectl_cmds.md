```sh
# Get the pods whose names match the pattern
kgp -n fedlearner-uat | awk '/filebeat/ {print $1}'

# Delete the pods whose names match the pattern
kgp -n fedlearner-uat | awk '/filebeat/ {print $1}' | xargs kubectl delete pods -n fedlearner-uat
```
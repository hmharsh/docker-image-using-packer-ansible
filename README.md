# Docker Image using Packer and Ansible
### To generate the docker image for the express app (app.tar.gz), install packer, docker and run 
```
# check the express application 
tar -zxf app.tar.gz
rm app.tar.gz
cd app

# compress express application back
tar -czf  app.tar.gz ./app

packer validate packer.json
packer build packer.json
# wait for some time
docker run -p 3000:3000 <image_id_form_build_log> &
```
Reference
https://ixis.co.uk/blog/pack-it-packaging-docker-images-packer#comment-1460
Classes That we need to make 
- [ ] Auth
- [ ] VPC
- [ ] Subnet
- [ ] AD
- [ ] S3
- [ ] Workspace
- [ ] Workspace Pool

- Auth should be able to log into aws and pass credentials in and tokens out. Holding onto the token timeout and warning when that will expire
- The AWS Services should adhere to the following abstract:
	- create_service(args) should go out cresate the service and return the json output and store that in some structure (TBD) so that it can be put into the {output_file}[obsidian://open?vault=100ftView&file=Conceptuals%2FSpecifics%2FLedger]
	- restart_service(args)should restart the service if it is in bad state, to be called if we run into issues automatically down the road manually in the short term
	- stop_service() stops the service
	- start_service() starts the service duh
	- destroy_service() this should both kill in the AWS instance and take out of output file
	- edit_service() if the service has anything it can change after creation allow here. 
	
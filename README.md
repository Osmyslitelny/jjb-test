# jjb-test

1) Up jenkins. `docker-compose up -d`
2) Update `user` & `password` into `jenkins_job.ini`
3) Put jobs into jobs folder
4) Command for running jjb:
For poweshell:
```
docker run --rm -v ${PWD}/jenkins_job.ini:/etc/jenkins_jobs/jenkins_jobs.ini -v ${PWD}/jobs:/opt/jobs -e PYTHONHTTPSVERIFY=0 osmman/jenkins-job-builder update -r /opt
```
# task-1 Explanation:

so here am using NODEJS Application.

first am taking a new server and it gives configurations like server name, ami:kernel 5.10, instance_type: t2.large, new_key_pair, new_security_group: its allows all traffic, EBS: 20GB.

after jenkins, docker, git tools setup and also am taking some security tools sonarqube, trivy, owasp.

jenkins setup after am access jenkins dashboard and am installed some plugins like Sonarqube Scanner, Eclipse Temurin Installer, NodeJs, OWASP Dependency-Check, Docker pipeline, Pipeline Stage View. After am integrating all plugins to the jenkins.

now am creating a new job

stage-1: clean workspace: to remove all files in the workspace before or after the build.

stage-2:  get the source code to ci server.

stage-3: here am using sonarqube analysis it is used to analyze source code, ensuring it adheres to coding standards and detecting bugs, code smells, and vulnerabilities.

stage-4: am using quality gate it is used to check the condition of that code if the code is must pass so to move the next stage of the pipeline. In-case if that code is errors so its not move the next stage of the pipeline and the pipeline also aborted.

stage-5: am using to build source code after the code is builed then installed dependencies.

stage-6: here am using OWASP security tool it is a OPEN WEB APPLICATION SOURCE PROJECT focuses on improving web application security.

stage-7: here am using  docker so am implementing dockerfile.
In dockerfile am using some commands like From, WorkDir, Run, Copy, Expose, CMD. and also am implementing slim images it is used to reduce the size of the image.
after am build the dockerfile. after dockerfile build is completed then image is created if it is to check docker images it is a command. so that iamge am pushing to dockerhub.

stage-8: here am using trivy tool. trivy tool is to scan the container images.

stage-9: After am deploying my application by using containers.

so this is my first task

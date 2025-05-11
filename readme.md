
## Tech stack


<h3 align="left">Languages and Tools:</h3>

<a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> 

<a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer"> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://hadoop.apache.org/" target="_blank" rel="noreferrer">  <a href="https://nodejs.org" target="_blank" rel="noreferrer"> 

## Start deploy 

**PowerShell commands - https://nodejs.org/en/download** (OPTIONAL)

````ps1
# Download and install fnm:
winget install Schniz.fnm

# Download and install Node.js:
fnm install 22

# Verify the Node.js version:
node -v # Should print "".

# Verify npm version:
npm -v # Should print "".

````

![Texto ](imgs/0.0.0.png)
![Texto ](imgs/0.0.1png)
![Texto ](imgs/0.0.2.png)
![Texto ](imgs/0.0.3.png)
![Texto ](imgs/0.0.4.png)
![Texto ](imgs/1.0.png)
![Texto ](imgs/1.1.png)
![Texto ](imgs/1.2.png)
![Texto ](imgs/1.3.png)
![Texto ](imgs/2.1.png)
![Texto ](imgs/2.png)
![Texto ](imgs/3.2.png)
![Texto ](imgs/3.3.png)
![Texto ](imgs/3.4.png)
![Texto ](imgs/3.5.png)
![Texto ](imgs/3.7.png)
![Texto ](imgs/3.8.png)
![Texto ](imgs/3.9.png)
![Texto ](imgs/3.10.png)
![Texto ](imgs/3.11.png)
![Texto ](imgs/3.12.png)


##  Read more:
- https://docs.aws.amazon.com/pt_br/elasticbeanstalk/latest/dg/create_deploy_nodejs.html
- https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/iam-instanceprofile.html
- [https://aws.amazon.com/pt/codepipeline/](https://aws.amazon.com/codepipeline/?nc1=h_ls)

Url para abrir no PC temporpario: http://calculadora-env-dev.eba-kp5bimrm.sa-east-1.elasticbeanstalk.com/

![Texto ](imgs/leituratemporaria.jpg)


## Next backend steps:
- If you update something in git, it will automatically update through the codepipeline.
- You can insert test phases in the middle, which avoids incorrect deployment, through buildspec.xml

````yml
version: 0.2

phases: 
    install:
        runtime-versions:
            nodejs: latest
        commands:
            - echo "installing something"
    pre_build:
        commands: 
            - echo "we are in the pre build phase"
    build:
        commands:
            - echo "we are in the build block"
            - echo "we will run some tests"
            - grep -Fq "Date Inicial:" index.html
            # se não tiver as palavras entre aspas não sobe para dev, ou stage ou prod errado
    post_build:
        commands:
            - echo "we are in the post build phase"
````            
- You can create three envs and orchestrate through aws organizations
<h3 align="left">Support:</h3>
<p><a href="#"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="Luiza" /></a></p><br><br>

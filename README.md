# A Rust CLI tool to deploy onto AWS

## Goal
* Build a cli tool with Rust
* Deploy the project onto AWS services, e.g. S3, Cloud9
* Learn AWS (probably leverage S3 and Cloud9) and Rust (mainly Clap in this project) as the project grows.

## Steps
* To first setup a lambda-rust installation env and enter that virtual environment, run  
```bash
python3 -m venv ~/.venv
source ~/.venv/bin/activate
```

* If you haven't installed python3, run
```bash
cd /
sudo apt-get install python3-venv
```

* To install _cargo-lambda_, run 
```bash
pip3 install cargo-lambda
```


* To create a lambda function, run
```bash
cargo lambda new [your_function_name]
```

* To Build and deploy your lambda functions, run
```bash
make release
```
, which is actually running ```cargo lambda build --release```

* To make an Amazon Linux 2 version release, run
```bash
make release-arm
```
, which is actually running ```cargo lambda build --release --arm64``` (see [Cross-compiling your lambda functions](https://github.com/awslabs/aws-lambda-rust-runtime#1-cross-compiling-your-lambda-functions))

## Roadmap
- [ ] Learn AWS through resources listed in References.
- [ ] Setup services.
- [ ] Deploy a cli tool

## Resources and References
- [ ] [AWS-S3-tutorial-for-beginners-official](https://www.youtube.com/watch?v=tfU0JEZjcsg)
- [ ] [AWS-Learner-lab](https://labs.vocareum.com/web/2370068/1491694.0/ASNLIB/public/docs/lang/en-us/README.html#envNav)
- [ ] [AWS-Setup-Credentials](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-credentials.html)
- [ ] [AWS-Learner-Lab](https://awsacademy.instructure.com/courses/37397)
* [Build-an-AWS-Lambda-Function-Deploy-in-Rust](https://www.youtube.com/watch?v=jUTiHUTfGYo)
* [Cloud-computing-for-data](https://paiml.com/docs/home/books/cloud-computing-for-data/)
* [rust-tutorial](https://nogibjj.github.io/rust-tutorial/chapter_1.html)
* [building-cloud-computing-solutions-at-scale-coursera](https://www.coursera.org/specializations/building-cloud-computing-solutions-at-scale)
* [rust-language-official-tool](https://doc.rust-lang.org/book/)
* [rust-cli-template](https://github.com/kbknapp/rust-cli-template)
* [command-line-rust](https://github.com/kyclark/command-line-rust)



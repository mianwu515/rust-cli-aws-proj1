
## Steps
* To first setup a lambda-rust installation env and enter that virtual environment, run  
```bash
python3 -m venv ~/.venv
source ~/.venv/bin/activate
```
* To exit the virtual environment
```bash
deactivate

# if it doesn't work, run this instead:
source deactivate
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

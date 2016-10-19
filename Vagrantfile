VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "dummy"
  config.vm.provider :aws do |aws, override|
    aws.access_key_id = "<>"
    aws.secret_access_key = "<>"
    aws.security_groups = ["default"] # Group names if default VPC, group IDs otherwise.
    aws.keypair_name = "terra1"
    aws.region = "us-east-1"
    aws.instance_type = "t2.micro"
    aws.ami = "ami-2d39803a"
    override.ssh.username = "ubuntu"
    override.ssh.private_key_path = "/root/.ssh/terra1.pem"
  end
end

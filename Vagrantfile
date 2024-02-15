require "vagrant-aws"
Vagrant.configure('2') do |config|
    config.vm.box='dummy'
    config.vm.provider 'aws' do |aws,override|
      aws.access_key_id=ENV['AWS_ACCESS_KEY_ID']
      aws.secret_access_key=ENV['AWS_SECRET_ACCESS_KEY']
      aws.keypair_name='ansiblekey'
      aws.instance_type='t2.micro'
      aws.region='eu-west-3'
      aws.availability_zone='eu-west-3c'
      aws.ami="ami-01d21b7be69801c2f"
      aws.security_groups='sg-036aeece823e623e2'
      aws.subnet_id="subnet-0adfe13e74fecacbb"
      override.ssh.username="ubuntu"
      override.ssh.private_key_path="~/ansiblekey.pem"
    end
end

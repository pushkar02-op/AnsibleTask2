- hosts: localhost
  vars_files:
          - vault.yml

  tasks:
          - name: Provision O.S
            ec2:
                    key_name: mykey121
                    aws_access_key: "{{ access_key }}"
                    aws_secret_key: "{{ secret_key }}"
                    instance_type: "t2.micro"
                    image: "ami-0447a12f28fddb066"
                    count: 1
                    assign_public_ip: yes
                    region: ap-south-1
                    wait: yes
                    vpc_subnet_id: "subnet-aa8da6c2"
                    state: present
                    group_id: "sg-01fff40f6be0c935b"
          - package:
                  name: httpd
                  state: present
          - copy:
                  src: test.html
                  dest: /var/www/var/html/
          - service:
                  name: httpd
                  state: started                                                                                                                                                         ~                                                                                                                                                           ~                                                                                                                                                           ~                                                                                                                                                           ~                                                                                                                                                           ~                                                                                                                                                           ~                                                                                                                                                           ~                                                                                                                                                           ~     

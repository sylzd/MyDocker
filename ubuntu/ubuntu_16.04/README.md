used to create a base system image by ubuntu:16.04 which can be connected by ssh!


run example:
$ sudo docker run -d -P --name test_sshd rastasheep/ubuntu-sshd:14.04
$ sudo docker port test_sshd 22
  0.0.0.0:49154

$ ssh root@localhost -p 49154
# The password is `root`
root@test_sshd $
# terraform
basic command
resource "aws_instance" "my_ec2_instance" {
        ami="ami-07d9b9ddc6cd8dd30"
        instance_type="t2.micro"
        tags={
        Name="terraformbatch"
}
}
output "ec2_public_ips" {
        value = aws_instance.my_ec2_instance.public_ip
}

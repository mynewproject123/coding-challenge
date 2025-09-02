**Terraform AWS VPC with EC2**

This project provisions an AWS infrastructure using Terraform. It creates:

     * A VPC with both public and private subnets across multiple availability zones.

     * An Internet Gateway for public subnets.

****A Security Group with the following rules:**
    * Port 80 (HTTP): Open to the world (0.0.0.0/0).

    * Port 22 (SSH): Restricted only to my IP address.

An EC2 instance in the public subnet, using the security group above.

We can further extend the current VPC with a NAT Gateway by assigning it an Elastic IP in the public subnet and configuring private route tables to route outbound traffic (0.0.0.0/0) through the NAT Gateway, allowing private subnets secure internet access without exposing them directly.

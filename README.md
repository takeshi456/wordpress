# Build WordPress quickly and more cheaper
Create WordPress platform by Cloudformation. EC2 and RDS under free tier.
I consider the portability of system so I choose to boot WordPress on Docker.([Docker Image](https://hub.docker.com/_/wordpress))

## Prerequisite
Check below envirionment.
- Create AWS Account.([Guide](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/?nc1=h_ls))
- Install AWS CLI on your machine.([Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html))
- Create IAM User or IAM Role for executing AWS CLI.([IAM user Creation Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html), [IAM role Creation Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html))

You only need to attach 'AWSCloudFormationFullAccess' which is AWS managed IAM policy to IAM role or user you created.

## How to use
Just execute AWS CLI below
```
aws cloudformation create-stack --stack-name wordpress --region ap-northeast-1 --template-body file://wordpress.yml
```
It takes 
After that, access to EC2 instance's Public IP address port 80.

## Author
* **Kento Kashiwagi** - [tuimac](https://github.com/tuimac)
If you have some opinion and find bugs, please post [here](https://github.com/tuimac/wordpress/issues).

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Future Plan
- Create backup and restore data automation tool
- Create notification for increacing price

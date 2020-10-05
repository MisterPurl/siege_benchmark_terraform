[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FMisterPurl%2Fsiege_benchmark_terraform&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
# siege_attack_terraform

Stresstest http or https on domain.tld/IP whith AWS t2.micro and siege tools (https://www.joedog.org/siege-home/)

## Configuration
### modify variables.tf file with your ID

```bash
variable "AWS_ACCESS_KEY_ID" {
    type = string
    default = "your"
}
variable "AWS_SECRET_ACCESS_KEY" {
    type = string
    default = "your"
}
```

### modify the target server

Modify the ligne whith the target :

```bash
sudo siege -c10 -r1000 http://THE_WEB_SITE
```

### Check and start the terraform

```bash
terraform init
terraform plan
terraform apply -auto-approve
```

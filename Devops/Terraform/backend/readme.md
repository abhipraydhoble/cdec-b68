```hcl
terraform {
  backend "s3" {
    bucket  = "cdec-b68-terraform-remote-backend"
    region  = "ap-southeast-1"
    key     = "terraform.tfstate"
    profile = "tf-user"
    dynamodb_table = "state_lock_tbl"
    #use_lockfile = true
  }
}
```
````
terraform init
````

- additonal commands
````
terraform init -reconfigure
````
````
terraform init -migrate-state
````

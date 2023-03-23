Terraform Basic Example

This folder contains a very simple Terraform module to demonstrate how you can use Terratest to write automated tests for your Terraform code. This module takes in an input variable called example, renders it using a template_file data source, and outputs the result in an output variable called example.

Check out test/terraform_basic_example_test.go to see how you can write automated tests for this simple module.

Note that this module doesn't do anything useful; it's just here to demonstrate the simplest usage pattern for Terratest. For a slightly more complicated, real-world example of a Terraform module and the corresponding tests, see terraform-aws-example.
Running this module manually

    Install Terraform and make sure it's on your PATH.
    Run terraform init.
    Run terraform apply.
    When you're done, run terraform destroy.

Running automated tests against this module

    Install Terraform and make sure it's on your PATH.
    Install Golang and make sure this code is checked out into your GOPATH.
    cd test
    dep ensure
    go test -v -run TestTerraformBasicExample

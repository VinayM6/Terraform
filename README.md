# Terraform
Terraform Insights 
# Terraform is logically split into two main parts: Terraform Core -----Remote procedure Call(RPC) interface-----> Terraform Plugins

# Terraform Core: 
This is the Terraform binary that communicates with plugins to manage infrastructure resources. It provides a common interface that allows you to leverage many different cloud providers, databases, services, and in-house solutions.
# Terraform Plugins:
Plugins are executable binaries written in Go that communicate with Terraform Core over an RPC interface. Terraform currently supports one type of plugin called providers. Each provider plugin exposes an implementation for a specific service or tool, such as the AWS provider or the cloud-init provider.

     Input       |---------------|    >---------------------------------------------->    |-------------------|
  |---------|    |---------------|    >---------------------------------------------->    |-------------------|
     Config      |#Terraform Core|    >-----Remote procedure Call(RPC) interface----->    |-Terraform Plugins-|
      File       |---------------|    >---------------------------------------------->    |-------------------|
       +         |               |    >---------------------------------------------->    |-------------------|
     State       |               |    >---------------------------------------------->    |-------------------|
     File        |---------------|    >---------------------------------------------->    |-------------------|
   |--------|    |---------------|    >---------------------------------------------->    |-------------------|

# WooCommerce Docker Compose set

Docker set for running WooCommerce instances.

## Requirements

- Git
- Latest Docker 
- Latest Docker Compose

## How to use

In terminal application clone current repository:

`git clone git@github.com/itembase/woocommerce-docker.git`

Change to the directory of the repository and switch to the folder of the desired WooCommerce and WordPress version:

`cd wp-x.x.x_wc-y.y.y`

where `x.x.x` can be `4.7.5`, `4.8.0` or `5.2.2` and `y.y.y` can be `2.6.14`, `3.1.0` and `3.6.5`. In selected folder 
run the following command:

`docker-compose up -d`

Wait while all containers will be up and running. As soon as all is up and running visit `http://localhost:8080` and 
follow the instructions to configure the installation.

After installation is completed log in as an admin. Navigate to "Plugins" section in the admin area 
(`http://localhost:8080/wp-admin/plugins.php`). Activate "WooCommerce" plugin. Follow wizard steps to configure 
WooCommerce.

You can disable:

- all payment options and just keep "Cache on delivery"
- disable "Print shipping labels at home"
- disable all enhancements from the "Recommended" tab
- skip "Jetpack"

## Reference

Based on https://hub.docker.com/_/wordpress and https://hub.docker.com/_/mysql Docker images.

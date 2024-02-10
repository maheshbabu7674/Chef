Certainly! Below is a list of commonly used Chef commands along with examples:

1. **Working with Cookbooks:**
   - `chef generate cookbook cookbook_name`: Create a new cookbook.
     ```bash
     chef generate cookbook my_cookbook
     ```

   - `chef generate recipe recipe_name`: Create a new recipe within a cookbook.
     ```bash
     chef generate recipe my_cookbook my_recipe
     ```

2. **Working with Nodes:**
   - `knife node list`: List all nodes registered with the Chef Server.
     ```bash
     knife node list
     ```

   - `knife node show node_name`: Display details about a specific node.
     ```bash
     knife node show my_node
     ```

3. **Working with Environments:**
   - `knife environment list`: List all environments.
     ```bash
     knife environment list
     ```

   - `knife environment show environment_name`: Display details about a specific environment.
     ```bash
     knife environment show development
     ```

4. **Bootstrap a Node:**
   - `knife bootstrap node_ip -x username -P password --sudo`: Bootstrap a node for Chef configuration.
     ```bash
     knife bootstrap 192.168.1.10 -x myuser -P mypassword --sudo
     ```

5. **Run Chef Client:**
   - `chef-client`: Run Chef Client manually on a node.
     ```bash
     chef-client
     ```

   - `chef-client -o "recipe[my_cookbook::my_recipe]"`: Run a specific recipe.
     ```bash
     chef-client -o "recipe[my_cookbook::my_recipe]"
     ```

6. **Upload Cookbooks:**
   - `knife upload /path/to/cookbooks`: Upload cookbooks to the Chef Server.
     ```bash
     knife upload /path/to/cookbooks
     ```

7. **Search Nodes:**
   - `knife search node 'platform:ubuntu'`: Search for nodes based on a query.
     ```bash
     knife search node 'platform:ubuntu'
     ```

8. **Role Management:**
   - `knife role list`: List all roles.
     ```bash
     knife role list
     ```

   - `knife role show role_name`: Display details about a specific role.
     ```bash
     knife role show webserver
     ```

9. **SSL Certificate Management:**
   - `knife ssl check`: Check SSL certificate validity.
     ```bash
     knife ssl check
     ```

   - `knife ssl fetch`: Fetch and update SSL certificates.
     ```bash
     knife ssl fetch
     ```

These are some of the basic Chef commands. The usage might vary depending on your specific configuration and requirements. Refer to the official Chef documentation for more detailed information on each command and its options.

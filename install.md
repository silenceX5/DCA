Installing Docker on Ubuntu 20.04 involves a series of steps to ensure you get the latest stable version. Here's a breakdown of the process, combining the information from the search results:

**1. Uninstall Old Versions (If Applicable):**

* If you have any previous Docker installations, it's a good practice to remove them to avoid conflicts:
    * `sudo apt-get remove docker docker-engine docker.io containerd runc`

**2. Update Package Repositories:**

* Ensure your system's package lists are up to date:
    * `sudo apt update`

**3. Install Required Packages:**

* Install packages that allow `apt` to use repositories over HTTPS:
    * `sudo apt install apt-transport-https ca-certificates curl software-properties-common`

**4. Add Docker's GPG Key:**

* Download and add Docker's GPG key to verify package authenticity:
    * `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

**5. Add the Docker Repository:**

* Add the official Docker repository to your system's sources:
    * `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"`
    * or, if you want to use the output of the lsb_release command to get the correct codename:
    * `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`

**6. Install Docker Engine:**

* Update the package index again, and then install Docker Engine, containerd, and Docker Compose:
    * `sudo apt update`
    * `sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin`

**7. Verify the Installation:**

* Check if Docker is running:
    * `sudo systemctl status docker`
* Run the "hello-world" container to test your installation:
    * `sudo docker run hello-world`
* Check the docker version.
    * `sudo docker version`

**Important Notes:**

* **sudo:** Most of these commands require `sudo` to run with administrator privileges.
* **Docker Desktop vs. Docker Engine:**
    * The instructions above install Docker Engine. If you are looking for Docker Desktop, which includes a GUI, then you will need to download the .deb file from the docker website, and install it. Docker Desktop is easier to use, but Docker engine is lighter weight, and better for servers.
* Always use the official Docker documentation as a primary source of information.

I hope this helps!

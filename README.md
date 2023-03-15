# Docker 101 - Hands On

**This Lab deploys a sinatra application to a K8S cluster in the cloud.**

## Getting started

- [Running the Sinatra App locally](#running-the-sinatra-app-locally)
- [Running the Sinatra App in a local container](#running-the-sinatra-app-in-a-local-container)

### Running the Sinatra App locally

Before you start, make sure you are using ruby version 3.1. You can check the version by running `ruby -v`.

1. Clone this repository:

   ```bash
    git clone git@github.com:HeitorMC/HandsOn-k8s.git
   ```

2. Change into the application directory:

   ```bash
    cd HandsOn-k8s
   ```

3. install the dependencies:

   ```bash
    bundle exec ruby app.rb
   ```

4. Run the app

   ```bash
    bundle exec ruby app.rb
   ```

5. The web application will be availabe at http://localhost:4567/

### Running the Sinatra App in a local container

1. Clone this repository:

   ```bash
    git clone git@github.com:HeitorMC/HandsOn-k8s.git
   ```

2. Change into the application directory:

   ```bash
    cd HandsOn-k8s
   ```

3. Build the app’s container image

   ```bash
    docker build -t sinatra-app .
   ```

4. Run the container

   ```bash
    docker run -p 4567:4567 sinatra-app
   ```

5. The web application will be availabe at http://localhost:4567/

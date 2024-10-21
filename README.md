# ATOC5051_F2024_activities_ECCO

## Running the notebooks

Notebooks for these activities are supported by a containerized environment; therefore, you'll need Docker to set them up, via the following:

1. Follow the install instructions for Docker on your operating system of choice: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/).
2. From your terminal, clone this repository:
   ```
   git clone https://github.com/donatagiglio/ATOC5051_F2024_activities_ECCO
   cd ATOC5051_F2024_activities_ECCO
   ```
3. Start the notebook server:
   ```
   docker container run -p 8888:8888 -v $(pwd):/books --name ecco argovis/ecco:241014
   ```
   **Note for Windows users**: substitute $(pwd) with the actual whole path in the command just above.
5. Wait a few seconds, and there will be a URL in your terminal output that starts with ` http://127.0.0.1:8888/tree?token=...`. Copy and paste that whole thing into your favorite web browser to access your notebooks. Leave this terminal window running while you work with your notebooks.
6. When finished, in a new terminal window, kill off your container:
   ```
   docker container stop ecco
   docker container rm -f ecco
   ```

> **help it doesn't work!** if you have problems starting your notebook container, make sure you aren't running any other Jupyter notebooks on your computer; collisions between notebook servers are the most common speedbump people have.

### Homework
* Don't forget to fill up the Weekly Journal! 

##### Basic
1. Read the “Docker getting started guide” (https://docs.docker.com/get-started/): Part1 Orientation and Part2 Container.
2. Create a new repository called `class4-homework`, and in it, put the following:
  - a LICENSE file (choose the MIT License from GitHub)
  - the `my_csv_reader.py` from class 3 homework (use yours OR the one provided in class)
  - the data file you used from class 3 homework 
  - a `Dockerfile` to run your project. The `Dockerfile` should be based on the ubuntu:latest image and should install python3, contain your python script from last class, and set it up to run the script as soon as the container is turned on. A few tips: use the `docker build` command to build your Dockerfile and the `docker run` command to run it. Also, in your `Dockerfile`, you'll need to use statements like `FROM`, `ADD`, `COPY`, `CMD` and `RUN` accordingly to how you want to build your image. For the data, the container should either contain the data file, or use `volume mounting` to find it outside your container.
  - a `README.md` containing instructions for A) building the `Dockerfile` into an image, and B) running the image you built
3. Research “Continuous Integration” and add a short summary in your `README.md` that summarizes it and mentions one tool that you can use for it. Even better if that tool integrates with GitHub.

##### Advanced
1. Adjust your `my_csv_reader.py` from last week to work on the dataset your selected for your project. This means you should either:
- make a new script, adjusting the new one to the right file
- refactor your script to be more “general” and accept the path to a file as input (this can be accomplished with the `argparse` library)
- feel free to also adjust your script to also use libraries now, such as `numpy`, `pandas`, and `csv`, they'll be the main topic of our next class!

##### Reach
1. Extend the `my_csv_reader.py` you modified in the `Advanced` section to compute the 
- mean of each feature in your dataset
- standard deviation of each feature in your dataset 

# build docker image
  docker build .

# build docker image passing file name
  docker build -f Dockerfile.dev .

# run docker image
  docker run 'imageid'

# map the port
  docker run -p 3000:3000 'imageid'

  docker run -p 3000:3000 b4b689ccc529

# Volumes setup

docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app 9a230bb482a3

# Run specific image command from docker

docker run 'imageid' npm run test

# Run specific image command from docker interactively (pseudo terminal)

docker run -it 'imageid' npm run test

# run tests on change with out docker compose

docker exec -it 'imageid' npm run test

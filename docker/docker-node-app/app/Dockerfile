# build a second container from the initial one
FROM node:latest as APPP

# set the work directory
WORKDIR /usr/src/app

# copy (source path and destination path)
COPY . .

# use a smaller node package
FROM node:alpine

# from initial (bigger, in development) container, copy the app into the second (smaller, in production) container
COPY --from=APPP /usr/src/app /usr/src/app


# set the work directory
WORKDIR /usr/src/app

# expose required port
EXPOSE 3001

# execute command (in this case running the app)
CMD ["node", "app.js"]

# tudortocan/docker-app
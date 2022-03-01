# image we created container from
FROM nginx

# label to comunicate to team members (optional)
LABEL MAINTAINER=tudortocan

# copy data from localhost to container
COPY index.html /usr/share/nginx/html

# expose port (whiever you want to use)
EXPOSE 80

# launch/create container which allows us to see app running in the browser
CMD ["nginx", "-g", "daemon off;"]
FROM node:14-alpine

# tz
ENV TZ Asia/Kolkata

# Current working directory
WORKDIR /app

COPY package*.json .
RUN npm install

COPY . .

ARG PORT=3000
ENV PORT $PORT
EXPOSE $PORT

ARG SQLITE_LOCATION=/etc/todos/todo.db
ENV SQLITE_DB_LOCATION=$SQLITE_LOCATION

CMD [ "node", "src/index.js" ]

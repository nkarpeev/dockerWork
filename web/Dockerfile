
FROM nginx:1.14-alpine

ARG WORKDIR

RUN rm /etc/nginx/conf.d/default.conf
COPY site.conf /tmp/site.conf

RUN cat /tmp/site.conf | sed -e "s|\$WORKDIR|${WORKDIR}|" > /etc/nginx/conf.d/site.conf \
    && rm /tmp/site.conf


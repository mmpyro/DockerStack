FROM fluent/fluentd:v0.12
WORKDIR /home/fluent
ENV PATH /home/fluent/.gem/ruby/2.3.0/bin:$PATH
ENV FLUENTD_CONF fluent.conf
USER root
RUN apk update && apk add make gcc libc-dev ruby-dev
RUN gem install fluent-plugin-concat
#RUN gem install fluent-plugin-mongo
RUN apk del gcc make libc-dev
EXPOSE 24224
CMD fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins $FLUENTD_OPT

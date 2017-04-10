FROM fluent/fluentd:v0.12

COPY my_fluent.conf /fluentd/etc/

USER root
RUN mkdir -p /pos/log/
RUN chown -R fluent:fluent /pos
USER fluent

ENV FLUENTD_OPT=""
ENV FLUENTD_CONF="my_fluent.conf"


CMD exec fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins $FLUENTD_OPT
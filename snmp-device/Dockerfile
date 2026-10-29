FROM alpine:3.20
RUN apk add --no-cache net-snmp
RUN printf 'rocommunity public default\nagentaddress udp:161\nsysName router-sim\nsysLocation Lab-Jakarta\n' > /etc/snmp/snmpd.conf
EXPOSE 161/udp
CMD ["snmpd","-f","-C","-Lo","-c","/etc/snmp/snmpd.conf"]

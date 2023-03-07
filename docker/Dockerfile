ARG JDK_VERSION=19-alpine3.17
FROM amazoncorretto:${JDK_VERSION}
ENV MINECRAFT_VERSION=1.19.3
ENV PAPER_VERSION=445
ENV XMX=-Xms2048M
WORKDIR /minecraft
ADD --chmod=775 https://api.papermc.io/v2/projects/paper/versions/${MINECRAFT_VERSION}/builds/${PAPER_VERSION}/downloads/paper-${MINECRAFT_VERSION}-${PAPER_VERSION}.jar ./mc.jar
COPY . .
EXPOSE 25565/tcp
EXPOSE 25565/udp
ENTRYPOINT [ "./entrypoint.sh" ]
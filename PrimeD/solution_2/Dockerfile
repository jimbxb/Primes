FROM alpine:3.13
COPY . /app
WORKDIR /app
RUN apk update \ 
    && apk add curl bash xz build-base ldc dub libgcc --no-cache \
    && dub build -b release --compiler=ldc2
ENTRYPOINT [ "./solution_2" ]
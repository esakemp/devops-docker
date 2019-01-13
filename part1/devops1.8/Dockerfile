FROM java:8

WORKDIR /mydir

RUN apt-get -y update

RUN apt-get -y install git

RUN git clone https://github.com/esakemp/Palindrome.git

WORKDIR /mydir/Palindrome/src/

RUN javac -cp . Main.java

CMD ["java", "Main"]

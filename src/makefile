flags=-std=c++11 -O2 -Wall

pcstats: main.o pcstats.o main_window.o
	g++ $(flags) -o pcstats main.o pcstats.o main_window.o -lncurses
	rm *.o

pcstats.o: pcstats.cc
	g++ $(flags) -c pcstats.cc
	
main_window.o: main_window.cc
	g++ $(flags) -c main_window.cc

main.o: main.cc
	g++ $(flags) -c main.cc

install: pcstats
	sudo cp pcstats /usr/bin
	sudo cp ../packages/pcstats.desktop /usr/share/applications

uninstall:
	sudo rm /usr/bin/pcstats
	sudo rm /usr/share/applications/pcstats.desktop

clean:
	rm pcstats

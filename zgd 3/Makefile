FLAGS = -pedantic-errors -std=c++11

screenwin.o: screenwin.cpp screenwin.h
	g++ $(FLAGS) -c $<

KeyboardWin.o: KeyboardWin.cpp KeyboardWin.h
	g++ $(FLAGS) -c $<

FlappyBird_map.o: FlappyBird_map.cpp FlappyBird_map.h
	g++ $(FLAGS) -c $<

main.o: main.cpp FlappyBird_map.h
	g++ $(FLAGS) -c $<

FlappyBird: KeyboardWin.o screenwin.o FlappyBird_map.o main.o
	g++ $(FLAGS) $^ -o $@ 

clean:
	rm -f *.o FlappyBird
	
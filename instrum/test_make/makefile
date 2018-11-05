perem = /home/01/kabanov/print_msg
perem1 = /home/01/kabanov/print_msg.1.gz
help:
	@echo Введите \"make all\" для сборки программы.
	@echo Введите \"make install\" для установки.
	@echo Введите \"make uninstall\" для удаления программы.
	@echo Введите \"make clean\" для удаления временных файлов.
	@echo Введите \"make distclean\" для полной очистки.
	@echo Введите \"make check\" для тестового запуска проекта.
	@echo Введите \"make dist\" для создания дистрибутива проекта.
	@echo Введите \"make man\" для просмотра мануала.

man:
	cat maindoc print_msgdoc > manual
all:
	cd ./src && make main
	cd ./doc && make all

install: ./bin/print_msg
	cp ./bin/print_msg $(perem)
	cp ./doc/print_msg.1.gz $(perem1)
dist:
	tar -cvf ../print_msg.tar ./
	gzip --best ../print_msg.tar

check:
	./test.sh

uninstall:
	rm $(perem)
	rm $(perem1)

clean:
	cd ./src && make clean
	cd ./doc && make clean

distclean:
	rm ./bin/print_msg
	make clean

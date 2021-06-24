# CLI

## ls(list)

- ls 명령어는 현재 작업중인 위치에 존재하는 파일 혹은 폴더 목록을 보여준다.
- `(백틱) 3개는 코드 블락을 생성

```bash
tjdgu@DESKTOP-9M7HBOU MINGW64 ~/Desktop/Github_Study
$ ls
test_folder/  text.txt
```



## cd(change directory)

- 현재 작업중인 디렉토리를 변경
- cd만 칠 경우 최상위 폴더로 변경
- pwd 현재 작업중인 디렉토리 표기
- cd {변경하고자 하는 디렉토리 이름}으로 디렉토리 변경
- 탭 키를 이용하면 존재하는 하위폴더 이름에 한해 자동생성 가능
- cd ..  현재 작업중인 폴더의 상위 폴더로 이동

```bash
tjdgu@DESKTOP-9M7HBOU MINGW64 ~
$ cd {direcotory name}
tjdgu@DESKTOP-9M7HBOU MINGW64 ~
$ cd desktop/Github_Study/
tjdgu@DESKTOP-9M7HBOU MINGW64 ~/desktop/Github_Study
$ cd .. # 내 상위 폴더로 이동, . : 현재 작업중인 폴더 표기
```



## mkdir(make directory)

- 폴더를 생성

```bash
tjdgu@DESKTOP-9M7HBOU MINGW64 ~/desktop/Github_Study
$ mkdir {directory name}
```



## touch

- 파일을 생성

```bash
tjdgu@DESKTOP-9M7HBOU MINGW64 ~/desktop/Github_Study
$ touch {file name}.{확장자}
```




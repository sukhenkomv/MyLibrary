# MyLibrary

Библиотека, в которой в модуле mylibrary объявлен класс 

class MyClassFromLibrary {
    fun getText(): String {
        return "Hello"
    }
}

Библиотека собирается и выкладывается в maven репозиторий

        repositories {
            maven {
                name = 'myRepo'
                allowInsecureProtocol = true
                url = uri("http://m2-repo.ntk.novotelecom.ru:8081/artifactory/internal/")
            }
        }

Собрать и опубликовать библиотеку можно командой в IDE

gradle publish

или в консоли

./gradlew publish

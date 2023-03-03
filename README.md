# Autorizador

> Aplicação responsável pela autorização de transações de cartão.

[![Java Version][java-image]][java-url]
[![Spring Version][spring-image]][spring-url]

Esta aplicação atua na camada API, e possui a responsabilidade de realizar uma série de verificações e análises. Essas também são conhecidas como regras de autorização.
Ao final do processo, o autorizador toma uma decisão, aprovando ou não a transação.

## Configuração de Desenvolvimento

### Build

Para fazer o build da aplicação deve ser executado o seguinte comando.

```sh
mvn clean install -U
```

### Executar

#### Intellij

No diretório raiz do projeto crie um novo diretório chamado __.run__, dentro deste novo diretório deve ser criado o arquivo __launch.run.xml__ com as configurações abaixo.

```xml
<component name="ProjectRunConfigurationManager">
    <configuration default="false" name="Launch Application" type="Application" factoryName="Application">
        <envs>
            <env name="SPRING_PROFILES_ACTIVE" value="local" />
        </envs>
        <option name="MAIN_CLASS_NAME" value="br.com.medelo.autorizador.Application" />
        <module name="autorizador" />
        <method v="2">
            <option name="Make" enabled="true" />
        </method>
    </configuration>
</component>
```

Para que essa configuração fique disponível menu de execução deve ser feito um build (CRTL+F9) do projeto.

#### Visual Studio Code

No diretório raiz do projeto crie um novo diretório chamado __.vscode__, dentro deste novo diretório deve ser criado o arquivo __launch.json__ com as configurações abaixo.

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "java",
      "name": "Launch Application",
      "request": "launch",
      "cwd": "${workspaceFolder}",
      "console": "internalConsole",
      "mainClass": "br.com.medelo.autorizador.Application",
      "projectName": "autorizador",
      "env": { "SPRING_PROFILES_ACTIVE": "local" }
    }
  ]
}
```

## Documentação

[Página do Projeto no Confluence][confluence]

<!-- Markdown link & img dfn's -->
[java-image]: https://img.shields.io/badge/Java-v17-green
[spring-image]: https://img.shields.io/badge/Spring--Boot-v2.3.5.RELEASE-green
[java-url]: https://docs.oracle.com/en/java/javase/17/
[spring-url]: https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-dependencies/2.3.5.RELEASE
[confluence]: 
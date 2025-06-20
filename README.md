            - nome: Configurar Java JDK
  usos: ações/setup-java@v3.14.1
  com:
    # A versão do Java a ser configurada. Aceita uma versão completa ou parcial do Java. Veja exemplos de sintaxe suportada no arquivo README.
    versão java: # opcional
    # O caminho para o arquivo `.java-version`. Veja exemplos de sintaxe suportada no arquivo README
    java-version-file: # opcional
    # Distribuição Java. Veja a lista de distribuições suportadas no arquivo README
    distribuição:
    # O tipo de pacote (jdk, jre, jdk+fx, jre+fx)
    java-pacote: # opcional, o padrão é jdk
    # A arquitetura do pacote (o padrão é a arquitetura do executor de ação)
    arquitetura: # opcional
    # Caminho para onde o JDK compactado está localizado
    jdkFile: # opcional
    # Defina esta opção se desejar que a ação verifique a versão mais recente disponível que atenda às especificações da versão
    check-latest: # opcional
    # ID do repositório distributionManagement no arquivo pom.xml. O padrão é `github`
    server-id: # opcional, o padrão é github
    # Nome da variável de ambiente para o nome de usuário para autenticação no repositório do Apache Maven. O padrão é $GITHUB_ACTOR
    server-username: # opcional, o padrão é GITHUB_ACTOR
    # Nome da variável de ambiente para senha ou token para autenticação no repositório Apache Maven. O padrão é $GITHUB_TOKEN
    server-password: # opcional, o padrão é GITHUB_TOKEN
    # Caminho para onde o arquivo settings.xml será gravado. O padrão é ~/.m2.
    settings-path: # opcional
    # Sobrescreva o arquivo settings.xml, se existir. O padrão é "true".
    overwrite-settings: # opcional, o padrão é verdadeiro
    # Chave privada GPG a ser importada. O padrão é uma string vazia.
    gpg-private-key: # opcional
    # Nome da variável de ambiente para a frase-senha da chave privada GPG. O padrão é $GPG_PASSPHRASE.
    gpg-passphrase: # opcional
    # Nome da plataforma de compilação para armazenar dependências em cache. Pode ser "maven", "gradle" ou "sbt".
    cache: # opcional
    # Solução alternativa para passar o status do trabalho para a etapa de publicação do trabalho. Esta variável não se destina à configuração manual.
    job-status: # opcional, o padrão é ${{ job.status }}
    # O token usado para autenticação ao buscar manifestos de versão hospedados em github.com, como para a compilação da Microsoft do OpenJDK. Ao executar esta ação em github.com, o valor padrão é suficiente. Ao executar em GHES, você pode passar um token de acesso pessoal para github.com se estiver enfrentando limitação de taxa.
    token: # opcional, o padrão é ${{ github.server_url == 'https://github.com' && github.token || '' }}
    # Nome do ID da cadeia de ferramentas Maven, caso o nome padrão "${distribution}_${java-version}" não seja desejado. Veja exemplos de sintaxe suportada no arquivo de Uso Avançado.
    mvn-toolchain-id: # opcional
    # Nome do fornecedor do Maven Toolchain, caso o nome padrão "${distribution}" não seja desejado. Veja exemplos de sintaxe suportada no arquivo de Uso Avançado.
    mvn-toolchain-vendor: # opcional
          

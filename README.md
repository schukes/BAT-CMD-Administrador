# Run CMD as Administrator (UAC Elevation via Batch Script)

Este é um script `.bat` que permite executar comandos com privilégios de administrador no Windows. Ele verifica se o script foi executado com permissões elevadas e, se não, utiliza um arquivo `.vbs` temporário para acionar a UAC e relançar o próprio script com permissões elevadas.

## Como funciona

- Verifica se o usuário tem privilégios administrativos
- Se não tiver, chama o prompt UAC para elevação
- Após a elevação, executa o comando desejado (`cmd.exe` por padrão)

## Uso

1. Baixe ou copie o conteúdo do arquivo `run-as-admin.bat`
2. Execute com um duplo clique ou via terminal
3. O prompt de elevação do Windows (UAC) será exibido
4. Após aceitar, um novo CMD será aberto com privilégios de administrador

## Personalização

Você pode substituir a linha final do script:

```bat
%windir%\system32\cmd.exe


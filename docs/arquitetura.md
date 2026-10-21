# 🏛️ Documentação de Arquitetura

## 1. Visão Geral
O aplicativo segue uma arquitetura em camadas estrita, garantindo baixo acoplamento e alta coesão entre a interface gráfica e os comandos de sistema.

## 2. Padrões de Projeto (Design Patterns)
* **Facade Pattern (`core/adb_client.py`):** Centraliza e padroniza toda a comunicação com o ADB, abstraindo o uso de `subprocess` e tratamento de exceções (Timeouts, FileNotFoundError).
* **Strategy Pattern (`services/`):** Permite isolar cada rotina de manutenção (ex: `TrimService`, `AdwareCleanerService`) em classes independentes.
* **Observer / Asynchronous Threading (`ui/`):** Garante que operações de longa duração via ADB executem em *Background Threads*, atualizando a interface gráfica em tempo real via callbacks de log.

## 3. Fluxo de Execução
1. A **UI** aciona o método de serviço.
2. O **Service** valida as regras de negócio e chama o `ADBClient`.
3. O **Core** executa o binário local na pasta `bin/` (ou fallback no PATH) e retorna a saída bruta.
4. O **Service** processa a saída e devolve para a **UI** exibir no terminal integrado.

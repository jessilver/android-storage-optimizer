# 🗺️ Roadmap do Projeto

## Versão 1.0 (MVP Atual)
- [x] Estrutura modular limpa (Core, Services, UI).
- [x] Cliente ADB encapsulado (Facade Pattern).
- [x] Binários ADB embarcados (Standalone).
- [x] Otimização de blocos de baixo nível (`fstrim` em `/data`, `/system`, `/cache`).

## Versão 1.1 (Próxima Sprint)
- [ ] **Módulo de Varredura de Apps de Terceiros:**
  - Implementar comando `pm list packages -3` para listar pacotes instalados por usuários/fontes externas.
  - Exibir tabela com o nome do pacote e status na interface gráfica.
- [ ] **Identificação e Remoção de Adwares:**
  - Adicionar rotina de filtragem de pacotes suspeitos.
  - Implementar comando de desinstalação segura (`adb uninstall <package>`).

## Versão 1.2 (Futuro)
- [ ] Relatório visual detalhado do espaço de armazenamento por partição.
- [ ] Limpeza de caches órfãos em diretórios comuns do usuário.

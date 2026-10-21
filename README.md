# 📱 Android Storage Optimizer (Standalone)

Uma ferramenta desktop leve, moderna e 100% offline projetada para otimizar, limpar e gerenciar dispositivos Android diretamente via ADB (Android Debug Bridge), sem dependência de nuvem, cadastros ou conexões com a internet.

---

## 🚀 Funcionalidades Atuais (MVP)
* **Limpeza de Blocos de Baixo Nível (TRIM):** Envia comandos `fstrim` seguros para as partições críticas (`/data`, `/system`, `/cache`) para recuperar performance e combater a ampliação de escrita (*write amplification*) em memórias UFS/Flash.
* **Binários Embarcados (True Standalone):** Não exige que o usuário instale o Android SDK ou configure variáveis de ambiente no computador. O executável traz o binário do ADB embutido.
* **Interface Moderna e Fluida:** Desenvolvida em Python com CustomTkinter, garantindo feedback visual em tempo real sem travamentos de tela (uso de concorrência com Threads).

---

## 🔮 Roadmap (Próximas Versões)
* [ ] Varredura e listagem de aplicativos de terceiros (`pm list packages -3`).
* [ ] Ferramenta de identificação e remoção segura de adwares e softwares indesejados.
* [ ] Relatórios detalhados de espaço livre por partição.

---

## 🛠️ Tecnologias Utilizadas
* **Python 3.10+**
* **CustomTkinter** (Interface Gráfica)
* **ADB (Android Debug Bridge)**

---

## ⚙️ Como Executar o Projeto Localmente

1. Clone o repositório:
```bash
 git clone [https://github.com/seu-usuario/android-storage-optimizer.git](https://github.com/seu-usuario/android-storage-optimizer.git)
 cd android-storage-optimizer
```

2. Instale as dependências:
```bash
pip install -r requirements.txt

```


3. Certifique-se de que os binários do ADB estão na pasta `bin/` ou instalados no PATH do sistema.
4. Ative a **Depuração USB** no seu celular, conecte-o ao computador e execute:
```bash
python main.py

```



---

## 📄 Licença

Distribuído sob a licença MIT. Sinta-se à vontade para contribuir!

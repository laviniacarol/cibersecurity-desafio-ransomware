Projeto pequeno para estudar como um script em Python pode criptografar/decriptografar um arquivo (propósito educacional).

---

## O que tem aqui
- `encrypter.py` — lê `teste.txt`, criptografa com AES-CTR (biblioteca `pyaes`), remove o arquivo original e grava `teste.txt.ransomwaretroll`.
- `decrypter.py` — (inverso) lê o arquivo `.ransomwaretroll`, decripta com a mesma chave e restaura o arquivo original.

> Observação: as chaves e comportamento estão hardcoded — é para aprendizado e **não** para uso em produção.

---

## Pré-requisitos
- Python 3.8+ instalado
- pip

---

## Instalação rápida (Linux / macOS)
```bash
# criar e ativar um ambiente virtual (opcional, recomendado)
python3 -m venv venv
source venv/bin/activate

# instalar dependência
pip install pyaes
No Windows (PowerShell):

powershell
Copiar código
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install pyaes
Como usar (passo a passo)
Coloque um arquivo chamado teste.txt na raiz do repositório (ou ajuste o nome no script).

Criptografar:

bash
Copiar código
python encrypter.py
Saída esperada: teste.txt.ransomwaretroll criado; teste.txt removido.

Decriptografar:

bash
Copiar código
python decrypter.py
Saída esperada: arquivo original restaurado (teste.txt ou similar, dependendo do script).

Detalhes técnicos rápidos
Algoritmo: AES no modo CTR (via pyaes).

Chave: hardcoded (b"testeransomwares").

Extensão do arquivo criptografado: .ransomwaretroll.

Avisos importantes
Projeto educacional. Não use em sistemas reais ou dados sensíveis.

Hardcode de chave e remoção automática do arquivo original tornam esse código inseguro e perigoso para produção.

Teste sempre em arquivos dummy.


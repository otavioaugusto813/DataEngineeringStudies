---
tag: python, computing, programming, computacao
---
# Nested context managers

Dois context managers aninhados podem aumentar a performance do código, já que os arquivos são abertos ao mesmo tempo.


``` python
def copy(src, dst):
    """Copia o conteúdo de um arquivo para outro
    
    Args:
    src (str): Nome do arquivo que será copiado
    dst (str): Onde salvar o novo arquivo"""

    #abrir ambos os arquivos ao mesmo tempo com um context manager aninhado
    with open(src) as f_src:
	    with open(dst, "w") as f_fst:
	        # Lê e salva cada linha, uma por vez, no novo arquivo
	        for line in f_src:
	            f_dst.write(line)    
```
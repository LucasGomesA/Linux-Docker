Para prosseguir, clone o repositório e acesse o diretório incluso:

Next, clone the repository and access the included directory as follows:

    git clone https://github.com/LucasGomesA/Linux-Docker.git
    
    depois:
    followed by:
    
    cd Linux-Docker

---
Compilando o programa eBPF (evita a necessidade de instalar localmente todas as dependências do eBPF):

Compiling the eBPF program (avoids needing to install all eBPF dependencies locally):

---

se não tiver entrado no diretório Linux-Docker, entre (cd */Linux-Docker);
    
if you are not inside the Linux-Docker directory, go to it (cd */Linux-Docker);

---
depois rode:

then run:
    
    ./compile.sh

---
O resultado que se espera ao rodar o código:

The expected result after running the code is:

    Success! xdp_drop.o created.🍻🍻🍻

(caso falhe, confira se você está dentro da pasta Linux-Docker e tente novamente)

(if it fails, check if you currently are inside the Linux-Docker directory and try again)

---

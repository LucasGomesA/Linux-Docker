<summary>Baixando e criando docker em máquinas do tipo linux;</summary>

<summary>Downloading and creating docker on linux machines;</summary>

<summary>Primeiramente, supondo que a máquina ja esteja ligada, acesse a prompt de comando através dos aplicativos;</summary>
<summary>Firstly, supposing the computer is already on, acess the command prompt through the apps menu;</summary>

<summary>No terminal, utilize o comando:</summary>
<summary>Inside the terminal, use the command:</summary>

    sudo apt update
---
se a última linha estiver com pacotes que possam receber um upgrade, use:
---
if the last line shows that there are packages that can be upgraded, use:
---
    sudo apt upgrade -y
---
espere até que o upgrade seja concluido, em seguida, baixe o docker para finalizar o preparo:
wait untill the upgrade has concluded, afterward, download the docker to finish the first steps:

    curl -fsSL https://get.docker.com | sh

depois:
then:

    sudo usermod -aG docker $USER
    ("$USER" corresponde ao usuário do prompt, não deve ser trocado)
    ("$USER" corresponds to the current user of the prompt, do not change)

finalmente:
lastly:

    bash -c "$(curl -sL https://get.containerlab.dev)"

Setup concluído!
Setup concluded!

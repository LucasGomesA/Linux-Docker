Atualmente, a topologia no código está no arquivo "lab-ebpf.clab.yml", dentro do diretório Linux-Docker;

Currently, the topology inside the code is in the file "lab-ebpf.clab.yml", inside the Linux-Docker directory;

---
A topologia atual é:

The current topology is:

    name: ebpf-lab
    
    topology:
      nodes:
        node-a:
          kind: linux
          image: nicolaka/netshoot:latest
          exec:
            - ip addr add 10.0.0.1/24 dev eth1
    
        node-b:
          kind: linux
          image: nicolaka/netshoot:latest
          # Mount the compiled object file into the node
          binds:
            - xdp_drop.o:/xdp_drop.o
          exec:
            - ip addr add 10.0.0.2/24 dev eth1
    
      links:
        - endpoints: ["node-a:eth1", "node-b:eth1"]

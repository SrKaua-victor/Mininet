# Trabalho – Topologia Linear com Mininet

**Aluno:** Kauã Victor Garcia Siecola  
**Data:** 21/10/2025

---

##  Descrição
Este projeto tem como objetivo criar uma **topologia linear com 6 switches** no Mininet, 
utilizando largura de banda de 25 Mbps e o controlador padrão. 
Foram realizados testes de conectividade e desempenho entre os nós.

---

##  Comandos Utilizados

| Etapa | Comando | Descrição |
|-------|----------|-----------|
| 1 | `sudo mn --topo linear,6 --mac --link tc,bw=25` | Criação da topologia linear |
| 2 | `dump` | Mostra IPs, MACs e portas |
| 3 | `pingall` | Teste de conectividade (0% dropped) |
| 4 | `h1 iperf -s -p 5555` | Servidor TCP |
| 5 | `h2 iperf -c 10.0.0.1 -p 5555 -t 15 -i 1` | Cliente TCP (15s / 1s report) |

---

##  Resultados
**Pingall:**  
0% dropped (30/30 received)  

**Iperf:**  
Throughput médio ≈ 25 Mbps  

---

##  Conclusão
A topologia linear foi configurada com sucesso, 
comunicando todos os hosts e mantendo a largura de banda configurada de 25 Mbps.

class Lista {
    constructor(data) {
        this.data = data;
        this.prox = null;
    }
}

class prioriade_liista {
    constructor() {
        this.topo = null;
    }

  
    append(data) {
        const newLista = new Lista(data);
        if (!this.topo) {
            this.topo = newLista;
            return;
        }

        let atual = this.topo;
        while (atual.prox) {
            atual = atual.topo;
        }
        atual.prox = newLista;
    }

    printList() {
        let atual = this.topo;
        while (atual) {
            console.log(atual.data);
            atual = atual.prox;
        }
    }
}


const prioriade_liista = new ProibidosList();
prioriade_liista.append("Fulano");
prioriade_liista.append("Ciclano");
prioriade_liista.append("Beltrano");


console.log("Lista de Proibidos:");
prioriade_liista.printList();# Enade

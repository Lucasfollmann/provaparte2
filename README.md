# provaparte2
# Arvore binária 
* Uma árvore binária é uma estrutura de dados caracterizada por: Ou não tem elemento algum. Ou tem um elemento distinto, denominado raiz, com dois ponteiros para duas estruturas diferentes, denominadas subárvore esquerda e subárvore direita.
![enter image description here](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Binary_tree.svg/200px-Binary_tree.svg.png)


 * **Exemplo de algoritmo em Java**
* public class Arvore {

    public No raiz;

    class No {
        Integer valor;
        No filhoEsquerdo;
        No filhoDireito;

        public No(Integer valor) {
            this.valor = valor;
        }
    }

    public No inserir(Integer valor) {
        return this.inserir(new No(valor), raiz);
    }

    private No inserir(No novo, No anterior) {
        if (raiz == null) {
            raiz = novo;
            return raiz;
        }

        if (anterior != null) {
            if (novo.valor <= anterior.valor) {
                anterior.filhoEsquerdo = this.inserir(novo, anterior.filhoEsquerdo);
            } else if (novo.valor > anterior.valor) {
                anterior.filhoDireito = this.inserir(novo, anterior.filhoDireito);
            } else {
                return null;
            }
        } else {
            anterior = novo;
        }

        return anterior;
    }
}

# Árvore Balanceada

Em ciência da computação, uma árvore binária de busca balanceada ou árvore binária de busca auto balanceada é qualquer árvore de busca binária que automaticamente mantém a sua altura pequena mesmo depois de sucessivas inserções e exclusões arbitrárias.![enter image description here](https://www.inf.ufsc.br/~aldo.vw/estruturas/avl6a.gif)

# Diferenças
Uma árvore binária balanceada é uma árvore binária na qual as alturas das duas sub árvores de todo nó nunca difere em mais de O balanceamento de um NÓ é definido como a altura de sua sub árvore esquerda menos a altura de sua sub árvore direita.

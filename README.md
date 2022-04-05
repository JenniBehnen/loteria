# Projeto Loteria
Este é um projeto de simulador de loteria, onde o usuário digita seis números e realiza um sorteio de outros números, 
semelhante a loteria, ao final o simulador verifica quantos números o usuário acertou.

## Tecnologia Utilizadas 
- **HTML:** Estrutura do site;
- __CSS:__ Estilização do site;
- *_JS:_* Funções do site;
- ~~BootStrap:~~ Não foi utilizado.

### Possíveis Melhorias
1. [X] Subir para GitHubPages;
2. [ ] Alterar os Alerts;
3. [ ] Utilizar o BootStrap;
4. [ ] Deixar responsivo.

### Disponibilizado em
[GitHubPage](https://jennibehnen.github.io/loteria/)

### Prints da tela
| ID | Primeira Tela| Segunda Tela | 
|----|--------------|--------------|
| 1 | Loteria Limpa | Loteria Preenchida |
| 2 | ![image](https://user-images.githubusercontent.com/100212625/161782455-e1594fd1-4cba-41e0-a4f6-355fed5b0164.png)

### Função Principal 
```
function sorteio(){
    var cont = 0
    numSort =[]
    while(cont < 6){
        let num = Math.random() * 60
        num = Math.ceil(num)
        if(!numSort.includes(num)){
            numSort[cont] = num
            console.log(numSort)
            cont ++
        }
        
    }

    document.getElementById("sorteados").innerHTML = numSort
    contAcertos()
}

function getValor(valor, pos){
    valor = Number(valor)
    if(valor <= 0 || valor > 60){
        alert("Numero invalido, digite um  entre 1 e 60")
        document.getElementById(`num${pos+1}`).value= ""
    }else if (numEsco.includes(valor)){
        alert("Numero repetido, escolha um outro valor")
        document.getElementById(`num${pos+1}`).value= ""
    }else{
        numEsco[pos] = valor
        console.log(numEsco)
    }
    
}

function contAcertos(){
    var contA = 0
    numEsco.forEach(function(value, index){
        if(numSort.includes(value)){
            contA++
        }
    })
    document.getElementById("acertos").innerHTML = contA
}

```

### comando git 
para iniciar o projeto 
```bash: 
git init
```


<?php

class animal {//criando uma class
    public $cor;
    //propriedade
    public $nome;
    //uma propriedade/metodo publico pode ser acessado de qualquer lugar
    private $peso;
    public function __construct($cor, $nome, $peso)
    //uma propriedade /metodo privado poder ser acessado
    // so pela propria classou pela class filhas
    {
        $this->cor = $cor;
        $this->nome= $nome;
        $this->peso = $peso;
    }

    public function fazerBarulho(){
        //construtor usado para inicializar objetos
        echo "barulho";
    }

public  function getpeso(){
    return $this->peso;
}

public function setnome($nome){
    $this->nome = $nome;
}


    
}

class gato extends animal{
    //class que herda as propriedade e metodos da class pai
 public function fazerbarulho(){
    //restitura de metodo existente na class pai,adaptada
    echo 'miau';
 }
}




$boi = new animal('preto', 'bandido', 500 );
//criaçao de um objeto do tipo animal
//passamos os valores nos parenteses para ativar o construtor
//gerando um objeto com propriedades preenchidos
echo $boi->cor;
//acessadoa uma propriedade publica
echo "<br>";
echo $boi->nome;
echo "<br>";
$boi->fazerBarulho();
//chamando a exuçao de um metodo
echo $boi->getpeso();
echo "<br>";
$boi->setnome("mimosa");
echo "<br>";
echo $boi->nome; 
echo "<br>";
$gato = new gato('amarelo','xanim', 2);
//criando objeto da classe gato(que herda da class animal)
echo $gato->nome;
//acessando uma propriedade publica do gato herdado da classe animal
echo "<br>";
$gato->fazerBarulho();


?>

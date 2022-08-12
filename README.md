# aula-12--08
//variáveis da bolinha
let xBolinha = 400;
let yBolinha = 200;
let diametro = 30;
let raio = diametro / 2 ;

//velocidade da bolinha
let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;

function setup() {
  createCanvas(800, 400);
}

function draw() {
 background(0);
  mostrabolinha();
  movimentabolinha(); 
  verificaColisaoBorda();
}             
   
function mostrabolinha(){         
circle (xBolinha,yBolinha, diametro);
}

function movimentabolinha(){
  xBolinha += velocidadeXBolinha;
  yBolinha+=velocidadeYBolinha;
}


 function verificaColisaoBorda(){
  if(xBolinha + raio> width||
    xBolinha - raio< 0){
    velocidadeXBolinha *= -1;
  }
  if(yBolinha + raio > height ||
     yBolinha - raio < 0){
    velocidadeYBolinha *= -1;
  }
 }
  
  
  

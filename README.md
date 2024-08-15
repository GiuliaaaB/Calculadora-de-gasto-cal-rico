# Calculadora-de-Gasto-Calorico
# Este programa usa a linguagem C e tem sua função calcular as calorias gastas no dia a dia de uma pessoa onde ele pergunta qual a idade, peso, sexo, o tipo de atividade (leve, moderada, intensa) sendo, leve: atividades como cozinhar, limpar a casa, cuidar de crianças, trabalhar sentado e caminhar até 1 hora por dia, moderada: inclui atividades como fazer 1 hora diária de corrida, ciclismo, natação ou dança, trabalhar como operário de construção, garçom, vendedor de porta em porta, carteiro ou entregador de mercadorias leves,  e intensa: atividades como natação, corrida, andar de bicicleta ou dançar 2 horas por dia, trabalhador rural que trabalha com instrumentos manuais e caminha longas distâncias várias horas por dia, ou entregador de mercadorias pesadas. Em seguida, o programa pergunta o peso desejado da pessoa, assim calculando quantas calorias ele precisa gastar em tantos dias para atingir seu objetivo. Para calcular as calorias foi utilizada as fórmulas obtidas através de estudos da Universidade Harvard e percebemos que os valores alteram de homem para mulher, varia de uma idade para outra e o peso modifica o resultado também, uma pessoa com mais peso gasta mais calorias em uma caminhada por exemplo do que uma pessoa com menos peso, então tivemos que ir adaptando nosso código para obter um resultado mais preciso colocando vários comandos switch case com diferentes fórmulas que dependem dessas variáveis. 
#include <stdio.h>
#include <math.h>
void gasto_feminino(int idade, float peso, char tipo_atividade,float *gasto_diario) {
  if (idade >= 0 && idade <= 3){
    switch(tipo_atividade){
      case 'L':
        *gasto_diario = (((58.317*peso)-31.1) * 1.55) -1000;
        break;
      case 'M':
        *gasto_diario = (((58.317*peso)-31.1)*1.84) -1000;
        break;
      case 'I':
        *gasto_diario = (((58.317*peso)-31.1)*2.2) -1000;
        break;
    }
  }
  else if (idade >= 4 && idade <= 10){
    switch(tipo_atividade){
      case 'L':
        *gasto_diario = (((20.315 * peso)+485.9) * 1.55) -1600;
        break;
      case 'M':
        *gasto_diario = (((20.315 * peso)+485.9)*1.84) -1600;
        break;
      case 'I':
        *gasto_diario = (((20.315 * peso)+485.9)*2.2) -1600;
        break;
    }
  }
  else if (idade >= 11 && idade <= 18){
    switch(tipo_atividade){
      case 'L':
        *gasto_diario = (((13.384 * peso)+692.6) * 1.55) -1800;
        break;
      case 'M':
        *gasto_diario = (((13.384 * peso)+692.6)*1.84) -1800;
        break;
      case 'I':
        *gasto_diario = (((13.384 * peso)+692.6)*2.2) -1800;
        break;
    }
  }
  else if (idade >= 19 && idade <= 30){
    switch(tipo_atividade){
      case 'L':
        *gasto_diario = (((14.818 * peso)+486.6) * 1.55) -2300;
        break;
      case 'M':
        *gasto_diario = (((14.818 * peso)+486.6)*1.84) -2300;
        break;
      case 'I':
        *gasto_diario = (((14.818 * peso)+486.6)*2.2) -2300;
        break;
    }
  }
  else if (idade >= 31 && idade <= 60){
    switch(tipo_atividade){
      case 'L':
        *gasto_diario = (((8.126 * peso)+845.6) * 1.55) -2600;
        break;
      case 'M':
        *gasto_diario = (((8.126 * peso)+845.6)*1.84) -2600;
        break;
      case 'I':
        *gasto_diario = (((8.126 * peso)+845.6)*2.2) -2600;
        break;
    }
  }
  else {
        switch(tipo_atividade){
          case 'L':
            *gasto_diario = ((9.082 * peso)+658.5) * 1.55;
            break;
          case 'M':
            *gasto_diario = ((9.082 * peso)+658.5)*1.84;
            break;
          case 'I':
            *gasto_diario = ((9.082 * peso)+658.5)*2.2;
            break;
        }
  }
}

  void gasto_masculino(int idade, float peso, char tipo_atividade,float *gasto_diario){
    if (idade >= 0 && idade <= 3){
      switch(tipo_atividade){
        case 'L':
          *gasto_diario = (((59.512 * peso)-30.4) * 1.55) -1000;
          break;
        case 'M':
          *gasto_diario = (((59.512 * peso)-30.4)*1.84) -1000;
          break;
        case 'I':
          *gasto_diario = (((59.512 * peso)-30.4)*2.2) -1000;
          break;
      }
    }
    else if (idade >= 4 && idade <= 10){
      switch(tipo_atividade){
        case 'L':
          *gasto_diario = (((22.706 * peso)+504.3)*1.55) -1400;
          break;
        case 'M':
          *gasto_diario = (((22.706 * peso)+504.3)*1.84) -1400;
          break;
        case 'I':
          *gasto_diario = (((22.706 * peso)+504.3)*2.2) -1400;
          break;
      }
    }
    else if (idade >= 11 && idade <= 18){
      switch(tipo_atividade){
        case 'L':
          *gasto_diario = (((17.686 * peso)+658.2) * 1.55) -2000;
          break;
        case 'M':
          *gasto_diario = (((17.686 * peso)+658.2)*1.84) -2000;
          break;
        case 'I':
          *gasto_diario = (((17.686 * peso)+658.2)*2.2) -2000;
          break;
      }
    }
    else if (idade >= 19 && idade <= 30){
      switch(tipo_atividade){
        case 'L':
          *gasto_diario = (((15.057 * peso)+692.2) * 1.55) -2000;
          break;
        case 'M':
          *gasto_diario = (((15.057 * peso)+692.2)*1.84) -2000;
          break;
        case 'I':
          *gasto_diario = (((15.057 * peso)+692.2)*2.2) -2000;
          break;
      }
    }
    else if (idade >= 31 && idade <= 60){
      switch(tipo_atividade){
        case 'L':
          *gasto_diario = (((11.472 * peso)+873.1)*1.55) -2300;
          break;
        case 'M':
          *gasto_diario = (((11.472 * peso)+873.1)*1.84) -2300;
          break;
        case 'I':
          *gasto_diario = (((11.472 * peso)+873.1)*2.2) -2300;
          break;
      }
    }
    else {
          switch(tipo_atividade){
            case 'L':
              *gasto_diario = ((11.711 * peso)+587.7)*1.55;
              break;
            case 'M':
              *gasto_diario = ((11.711 * peso)+587.7)*1.84;
              break;
            case 'I':
              *gasto_diario = ((11.711 * peso)+587.7)*2.2;
              break;
          }
    }
  } 

int main(void) {
  int idade,dias;
  float peso_atual,peso_desejado,peso_final,gasto_diario,gasto_total,gasto_em_kilos;
  char Sexo,tipo_atividade;

  printf("Ola seja bem vindo(a) a nossa calculadora de gasto calorico!\n");
  printf("Para comecar digite a sua idade e peso:\n");
  scanf("%d %f", &idade, &peso_atual);

  printf("Agora digite o seu sexo, sendo F para feminino e M para masculino:\n");
  scanf(" %c", &Sexo);

  printf("\nAgora informe qual tipo de atividade voce faz, aqui vai uma breve explicacao ->\n" "\nLeve: considera atividades como cozinhar; limpar a casa; cuidar de criancas; trabalhar sentado e caminhar ate 1 hora por dia.\n"
    "\nModerada: inclui atividades como fazer 1 hora diaria de corrida, ciclismo, natacao ou danca; trabalhar como operario de construcao, garcom, vendedor de porta em porta, carteiro ou entregador de mercadorias leves\n"
    "\nIntensa: considera atividades como natacao, corrida, andar de bicicleta ou dançar 2 horas por dia; trabalhador rural que trabalha com instrumentos manuais e caminha longas distancias, varias horas por dia; ou entregador de mercadorias pesadas\n" 
    "\nsendo 'L'' para Leve, 'M' para Moderada ou 'I' para Intensa\n");
  scanf(" %c",&tipo_atividade);
  printf("\nAgora informe o seu peso desejado:\n");
  scanf("%f",&peso_desejado);
  peso_final= peso_atual - peso_desejado;

  if (Sexo == 'F') {
      gasto_feminino(idade, peso_atual, tipo_atividade,&gasto_diario);
  } 
  else if (Sexo == 'M') {
      gasto_masculino(idade, peso_atual, tipo_atividade,&gasto_diario);
  };
  gasto_diario = round(gasto_diario);
  gasto_em_kilos = gasto_diario/7700.0;
  dias = 0;
  if (peso_desejado != peso_atual) {
    printf("Parabens, seu gasto calorico foi de %.2f calorias, em kilos %.2fkg! \n", gasto_diario, gasto_em_kilos);
      printf("Se continuar assim você atingirá seu peso em %d dias.\n", (int)(peso_final / gasto_em_kilos));
  } else if (peso_desejado == peso_atual) {
    printf("Você já atingiu o peso desejado!\n");
  }
  return 0;
}

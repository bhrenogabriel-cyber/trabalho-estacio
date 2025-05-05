#include <stdio.h>

int main(){

    char estado1[3], estado2[3];
    char cidade1[100], cidade2[100];
    char codigo1[50], codigo2[50];
    unsigned int populacao1, populacao2;
    float pontosturisticos1, pontosturisticos2;
    float pib1, pib2, area1, area2;
    float densidade1, densidade2;
    float riqueza1, riqueza2;
    float percpita1, percpita2;
    float superpoder1, superpoder2;
    int escolha;
    float atributo;
    //carta 1
    printf("...carta 1... \n");
    printf("Digite o estado (letra A a H):");
    scanf("%s", estado1);

    printf("Digite a cidade:");
    scanf("%s", cidade1);

    printf("Digite o codigo (ex: B10, A10):");
    scanf("%s", codigo1);

    printf("Digite a populacao:");
    scanf("%u", &populacao1);

    printf("Digite os pontos turisticos:");
    scanf("%f", &pontosturisticos1);

    printf("Digite o pib:");
    scanf("%f", &pib1);

    printf("Digite a area:");
    scanf("%f", &area1);

    densidade1 = populacao1 / area1;
    riqueza1 = pib1 / populacao1;
    percpita1 = pib1 / densidade1;
    superpoder1 = populacao1 + area1 + pib1 + pontosturisticos1 + riqueza1 + (area1 / populacao1);

    //carta 2
    printf("\n Carta 2: \n");
    printf("Digite a cidade (letra A a H):");
    scanf("%s", cidade2);

    printf("Digite o estado: ");
    scanf("%s", estado2);

    printf("Digite o codigo (ex: B10, A10):");
    scanf("%s", codigo2);

    printf("Digite a populacao:");
    scanf("%u", &populacao2);

    printf("Digite os pontos turisticos:");
    scanf("%f", &pontosturisticos2);

    printf("Digite o pib:");
    scanf("%f", &pib2);

    printf("Digite a area:");
    scanf("%f", &area2);

    densidade2 = populacao2 / area2;
    riqueza2 = pib2 / area2;
    percpita2 = pib2 / densidade2;
    superpoder2 = populacao2 + area2 + pib2 + pontosturisticos2 + riqueza2 + (area2 / populacao2);

    printf("\n carta 1 \n ");
    printf("Cidade: %s \n", cidade1);
    printf("Estado: %s \n", estado1);
    printf("Codigo: %s \n", codigo1);
    printf("Populacao: %u \n", populacao1);
    printf("Pontos turisticos: %.2f \n", pontosturisticos1);
    printf("Pib R$: %.2f \n", pib1);
    printf("Area: %.2f \n", area1);
    printf("Densidade: %.2f \n", densidade1);
    printf("Riqueza R$: %.2f \n", riqueza1);
    printf("Percpita: %.6f \n", percpita1);
    printf("Super poder: %.2f \n\n", superpoder1);

    printf("Carta 2\n ");
    printf("Estado: %s \n", estado2);
    printf("Cidade: %s \n", cidade2);
    printf("Codigo: %s \n", codigo2);
    printf("Populacao: %u \n", populacao2);
    printf("Pontos turisticos: %.2f \n", pontosturisticos2);
    printf("Pib R$: %.2f \n", pib2);
    printf("Area: %.2f \n", area2);
    printf("Densidade: %.2f \n", densidade2);
    printf("Riqueza R$: %.2f \n", riqueza2);
    printf("Percpita: %6.f \n", percpita2);
    printf("Super poder: %.2f \n\n", percpita2);

    // coparaçao das cartas

    printf(" ==== comparaçao das cartas ==== \n");
    printf("Populacao: %d \n", populacao1 > populacao2);
    printf("Pontos turisticos: %d \n", pontosturisticos1 > pontosturisticos2);
    printf("Area: %d \n", area1 > area2);
    printf("Pib: %d \n", pib1 > pib2);
    printf("Densidade (o menor vence): %d \n", densidade1 < densidade2);
    printf("Riqueza: %d \n", riqueza1 > riqueza2);
    printf("Percpita: %d \n ", percpita1 > percpita2);
    printf("Super poder: %d \n\n", superpoder1 > superpoder2);

    
    
    if (superpoder1 > superpoder2) {
        printf("Carta 1 vence \n ");

    }else
    {
     printf("Carta 2 vence.\n");
    }

    printf("### Escolha um atributo para comparar ###\n");
    printf("1 :populacao\n");
    printf("2. pib \n");
    printf("3. area \n");
    printf("4 densidade:\n");
    scanf("%d", &escolha);
   

    switch(escolha)
    {
    case 1: 
    if(populacao1 > populacao2){
     printf("### carta1 venceu ###");
    }
    else if (populacao1 < populacao2){
    printf("### carta 2 vence ###");
    }
    else {
    printf("### empate ###");
    }
    break;
    case 2: 
    if(pib1 > pib2){
     printf("### carta1 venceu ###");
    }
    else if (pib1 < pib2){
    printf("### carta 2 vence ###");
    }
    else {
    printf("### empate ###");
    }
    break;
    case 3: 
    if(area1 > area2){
     printf("### carta1 venceu ###");
    }
    else if (area1 < area2){
    printf("### carta 2 vence ###");
    }
    else {
    printf("### empate ###");
    }
    break;
    case 4: 
    if(densidade1 < densidade2){
     printf("### carta1 venceu ###");
    }
    else if (densidade1 < densidade2){
    printf("### carta 2 vence ###");
    }
    else {
    printf("### empate ###");
    }
    break;
    default: printf("opcao invalida!");



    return 0;
}}

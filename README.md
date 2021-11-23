#include<iostream>
#include<fstream>
using namespace std;
struct notas{
	float prova1;
	float aep1;
	float prova2;
	float aep2;
	float media1;
	float media2;
};
  
  
  #include "nota.h"

int main(){
	
	notas alunos;
	
	cout << "Nota da aep1: ";
	cin >> alunos.aep1;
	cout << "Nota da prova1: ";
	cin >> alunos.prova1;
	cout << "Nota da aep2: ";
	cin >> alunos.aep2;
	cout << "Nota da prova2: ";
	cin >> alunos.prova2;
	
	alunos.media1 = alunos.aep1 + alunos.prova1;
	alunos.media2 = alunos.aep2 + alunos.prova2;
	
	if(alunos.media1 < 6.0 && alunos.media2){
		cout << "Aluno reprovado.";
	}else{
		cout << "Aluno aprovado.";
	}
	
	ofstream arquivo;
    arquivo.open("alunos.ods", std::fstream::app);
	arquivo << alunos.aep1 << ";" << alunos.prova1 << alunos.aep2 << alunos.prova2 << "\n";
    arquivo.close();
	
	return 0;
}
  
  

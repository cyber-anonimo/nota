#include<iostream>
#include<fstream>
using namespace std;

struct Alunos{
	string nome;
	int matricula;
}typedef Alunos;

struct Notas{
	string nome;
	float aep1;
	float prova1;
	float aep2;
	float prova2;
	float media1;
	float media2;
	float mediaFinal;
	float sub1;
	float sub2;
}typedef Notas;

int CadastrarAlunos();

void arquivo(Notas aluno);

int CadastrarNotas();

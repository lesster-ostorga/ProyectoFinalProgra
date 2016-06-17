                                      //Para el primer archivo .h (pilas)
#include <iostream>
#include <stdio.h>
#include <stdlib.h>

using namespace std;

struct pila {
	char letra;
	pila * siguiente;
};

pila * iniciar;
pila * auxi;
pila * final;


void Apilar(char letra2){
	if (iniciar==NULL){
		iniciar= new(pila);
		iniciar->letra=letra2;
		final=iniciar;
	}else{
		auxi=new(pila);
		auxi->siguiente=iniciar;
		auxi->letra=letra2;
		iniciar=auxi;
	}
	final->siguiente=NULL;
}



void MostrarT(){
	auxi= iniciar;
	if(iniciar==NULL){
		cout <<"No hay nodos apilados" << endl;
	}else{
		while (auxi != NULL ){
			cout <<auxi->letra<< endl;
			auxi = auxi->siguiente;

	}
}
}

void Adesapilar(){
	auxi= iniciar;
	if(iniciar==NULL){
		cout <<"No hay nodos apilados" << endl;
	}else{
		if(auxi != NULL ){
			cout <<auxi->letra<< endl;
		}
	}
}


void Desapilar(){
	struct pila *pant=NULL;
	if (iniciar==NULL){
		cout<<"No hay nodos apilados" << endl;
	}
	else {
		auxi=iniciar;
		iniciar=iniciar->siguiente;
		pant=auxi;
		pant->siguiente=auxi->siguiente;

	}
}

void Tamanno(){
	int contador=0;
	auxi= iniciar;
	if(iniciar==NULL){
		cout <<"No hay nodos apilados" << endl;
	}else{
		while (auxi != NULL ){
            contador++;
			auxi = auxi->siguiente;
	}
	cout<<"Nodos apilados  "<<contador<<endl;
}
}



                                          //Para el segundo archivo .h (colas)
#include <iostream>
#include <stdio.h>
#include <stdlib.h>
using namespace std;



struct cola {
	char letra;
	cola * siguiente;
};

cola * inicio;
cola * auxiliar;
cola * fin;

void Push(char letra2){
	if (inicio==NULL){
		inicio= new(cola);
		inicio->letra=letra2;
		fin=inicio;
	}else{
		auxiliar=new(cola);
		fin->siguiente=auxiliar;
		auxiliar->letra=letra2;
		fin=auxiliar;
	}
	fin->siguiente=NULL;
}

void Mt(){
	auxiliar= inicio;
	if(inicio==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		while (auxiliar != NULL ){
			cout <<auxiliar->letra<< endl;
			auxiliar = auxiliar->siguiente;

	}
}
}

void Top(){
	auxiliar= inicio;
	if(inicio==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		if(auxiliar != NULL ){
			cout <<auxiliar->letra<< endl;
		}
	}
}

void Pop(){
	struct cola *pant=NULL;
	if (inicio==NULL){
		cout<<"No hay nodos encolados" << endl;
	}
	else {
		auxiliar=inicio;
		inicio=inicio->siguiente;
		pant=auxiliar;
		pant->siguiente=auxiliar->siguiente;

	}
}

void Tam(){
	int contador=0;
	auxiliar= inicio;
	if(inicio==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		while (auxiliar != NULL ){
            contador++;

			auxiliar = auxiliar->siguiente;
	}
	cout<<"Nodos encolados  "<<contador<<endl;
}
}



                                          Para el archivo .cpp (donde llamamos nuestras bibliotecas)

//============================================================================
// Name        : ProyectoFinalProgra.cpp
// Author      : lester Ostorga
// Version     :
// Copyright   : Your copyright notice
// Description : Hello World in C++, Ansi-style
//============================================================================

#include <iostream>
#include "colas.h"
#include "pilas.h"
using namespace std;

int main() {
	/*       funciones para Cola:
	 * 
	 * Push: ingresa un nuevo nodo.
	 * Pop: elimina el primer nodo que se ingreso.
	 * Top: muesta el Nodo a eliminar.
	 * Mt: muestra todos los nodos encolados.
	 * Tam: muetra cuantos nodos estan encolados.
	 *
	 *
	 *
	 *        funciones para Pila:
	 *        
	 * Apilar: ingresa un nuevo nodo.
	 * Desapilar: elimina el utimo nodo que se ingreso.
	 * Adesapilar: muesta el Nodo a eliminar.
	 * MostrarT: muestra todos los nodos encolados.
	 * Tamanno: muetra cuantos nodos estan encolados
	 *
	 */
	 return 0;
}


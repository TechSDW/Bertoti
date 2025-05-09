## Texto 1

Programação e engenharia de software são termos que possuem a mesma definição mesmo sendo diferente um do outro e muitos estudantes da área acabam conseguindo trabalhos como programador. 

Assim como na programação, a engenharia de software atual não possui respostas exatas, diferentemente de outros tipos de engenharia, onde um erro de cálculo pode causar um grande estrago. 

Mesmo que dois códigos distintos cujo propósito é igual, seja um com mais instruções que o outro, contanto que cheguem no resultado desejado podem ser considerados respostas certas, ainda que haja uma probabilidade de erro maior no futuro.

## Texto 2

Engenheiros de software visam utilizar ferramentas e processos para que um código consiga continuar a satisfazer a organização, ou seja, eles são responsáveis por manter e atualizar um código para que ele consiga continuar a realizar uma função desejada.

# Trade Off

Vários softwares são criados tentando atingir um certo objetivo para seu público alvo, como um aplicativo para organizar tarefas de uma empresa, todos os aplicativos mais famosos possuem alguma ferramenta que os diferem, dependendo da necessidade da organização eles irão escolher uma delas para implementá-la em sua empresa, esse é o trade off.

## Exemplos

**_Sistemas Operacionais:_**
O custo de um sistema operacional pode ser considerado um trade off, pois se deseja certas ferramentas que um SO gratuito não oferece, você terá que investir em algum como o Windows, por exemplo.
> O windows possui sua versão gratuita, porém para ter maior acesso, terá que pagar um valor

**Windows:**
Possui uma interface mais amigável, exibindo vários ícones, e sua interação não necessita do prompt de comando. Além disso, como possui várias funções, acaba se tornando mais pesado que o Linux.

**Linux:**
Para algumas tarefas, o Linux precisa que você digite alguns comandos para realizar certas tarefas, mas como ele é mais personalizável do que o Windows.

**_Linguagens de programação:_**
Complexidade entre Python e C, por exemplo. Cada vez que a linguagem fica mais distante da linguagem nativa (hardware), ela acaba se tornando menos complexa, porém mais lenta.

**Python:**
Para iniciantes, o python é menos complicado que C, mas acaba sendo mais lento.

**C:**
Linguagem usada para aplicativos relacionados ao hardware.

## Imagem metodologia ágil

![Image](https://github.com/user-attachments/assets/e093b8a0-cdc6-4943-8d1b-3b9e4ca4987a)

Esta imagem representa uma metodologia ágil, nela é possível notar que em todas as etapas do processo são entregas com uma funcionalidade para o cliente.

Com a metodologia ágil cada entrega possui um valor para o cliente, invés de fornecê-lo com algo útil apenas na última entrega.

# Exercício 5

## Classe

package Capivaras;

public class Capivara {
	private static String nome;
	private String cor;
	private String acessorio;
	private double peso;
	
	public Capivara(String nome, String cor, String acessorio, double peso) {
		this.nome = nome;
		this.cor = cor;
		this.acessorio = acessorio;
		this.peso = peso;}
	
	public static String getNome() {
		return nome;}
	public void setNome(String nome) {
		this.nome = nome;}
	
	public String getCor() {
		return cor;}
	public void setCor(String cor) {
		this.cor = cor;}
	
	public String getAcessorio() {
		return acessorio;}
	public void setAcessorio(String acessorio) {
		this.acessorio = acessorio;}
	
	public double getPeso() {
		return peso;}
	public void setPeso(double peso) {
		this.peso = peso;}
}

## Classe estacionamento

package Capivaras;

import java.util.List;
import java.util.LinkedList;

public class Parque {
	private List<Capivara> capivaras = new LinkedList<Capivara>();
	
	public void addCapivara(Capivara capivara) {
		capivaras.add(capivara);}
	
	public Capivara buscaNome(String nome) {
		for(Capivara capivara:capivaras) {
			if(Capivara.getNome().equals(nome)) return capivara;}
		return null;
	}
	
	public List<Capivara> buscaCor(String cor){
		List<Capivara> encontrados = new LinkedList<Capivara>();
		for(Capivara capivara: capivaras) {
			if(capivara.getCor().equals(cor)) encontrados.add(capivara);}
		return encontrados;
	}
	
	public List<Capivara> buscaAcessorio(String acessorio){
		List<Capivara> encontrados = new LinkedList<Capivara>();
		for(Capivara capivara: capivaras) {
			if(capivara.getAcessorio().equals(acessorio)) encontrados.add(capivara);}
		return encontrados;
	}
	
	public List<Capivara> buscaPeso(double peso){
		List<Capivara> encontrados = new LinkedList<Capivara>();
		for(Capivara capivara: capivaras) {
			if(capivara.getPeso() == peso) encontrados.add(capivara);}
		return encontrados;
	}
	
	public List<Capivara> getCapivara(){
		return capivaras;
	}
}

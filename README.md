package aula20;

import java.util.Scanner;

public class IMC {
	

	public static void main(String[] args)
	{
		Scanner ler=new Scanner(System.in);
		float peso,altura;
		float imc;
		System.out.println("peso da Pessoa (kg): ");
		peso = ler.nextFloat();
		System.out.println("altura da Pessoa (kg): ");
		altura = ler.nextFloat();
		imc =calcIMC(peso,altura);
		System.out.println("resultado do IMC: " + resultadoIMC(imc));
		ler.close();
		System.exit(0);
		}
	
	public static float calcIMC(float x,float y)
	{
		return (x/ (y*y));
	}
	
	public static String resultadoIMC(float imc)
	{
		String result;
		
		if (imc <=12)
			result = "abaixo do peso";
		else if (imc <=25)
			result = "peso ideal";
		else if (imc <=30)
			result = "acima do peso";
		else if (imc <=35)
            result= "Obesidade leve";
		else 
			result = "Obesidade";
		return result;
	}
		
	}
	

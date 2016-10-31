import java.util.Scanner;
public class DorniTutoriales {
	public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        //Variables
        int piedra = 0, papel = 1, tijera = 2, x = 0;
        int maquina = (int) (Math.random()*3+0);//numero aleatorio del 0 al 2
        int Usuario;
        int opcionUsuario;
        int contador=0;
        do{
            System.out.println("Elija de las siguientes opciones");
            System.out.println("1 - Empezar partida");
            System.out.println("2 - Instrucciones");
            System.out.println("3 - Salir del juego");
            System.out.println("4 - Creditos");
            opcionUsuario = entrada.nextInt();
            switch (opcionUsuario){
            case 1:
             do{
                    System.out.println("Elija una de las siguientes opciones");
                    System.out.println("0 - Piedra");
                    System.out.println("1 - Papel");
                    System.out.println("2 - Tijera");
                    Usuario = entrada.nextInt();
                        if(maquina == 0){
                            System.out.println("La maquina eligio piedra");
                        }else if(maquina == 1){
                            System.out.println("La maquina eligio papel");
                        }else if(maquina == 2){
                            System.out.println("La maquina eligio tijera");
                        }

                    //Condiciones
                        if(Usuario == piedra){
                            System.out.println("Tu elegiste piedra");
                            if (maquina == piedra){
                                System.out.println("Empate");
                            }else if(maquina == papel){
                                System.out.println("Has perdido");
                            }else if(maquina == tijera){
                                System.out.println("Tu Ganas");
                            }        
                        }else if(Usuario == papel){
                            System.out.println("Tu elegiste papel");
                            if (maquina == piedra){
                                System.out.println("Tu Ganas");
                            }else if(maquina == papel){
                                System.out.println("Empate");
                            }else if(maquina == tijera){
                                System.out.println("Has perdido");
                            }        
                        }else if(Usuario == tijera){
                            System.out.println("Tu elegiste tijera");
                            if (maquina == piedra){
                                System.out.println("Has Perdido");
                            }else if(maquina == papel){
                                System.out.println("Tu Ganas");
                            }else if(maquina == tijera){
                                System.out.println("Empate");
                            }        
                        }  
                else if(opcionUsuario == 2){
                    System.out.println("Instrucciones del juego:");
                    System.out.println("Tienes que elegir entre piedra, papel o tijera.");
                    System.out.println("La piedra vence a la tijera.");
                    System.out.println("La tijera vencen al papel.");
                    System.out.println("Y el papel vence a la piedra.");
                    System.out.println("Si ganas 5 tiradas ganas 1 ronda.");
                }else if(opcionUsuario == 3){
                    System.out.println("Abandonando juego...");
                    x=1;
                }else if(opcionUsuario == 4){
                	System.out.println("Hecho por:");
                	System.out.println("Federico Labrador");
                	System.out.println("Juan Arnaldi");
                	System.out.println("Nicolas Larrosa");
                }
                }while(x!=0);
             }
        }while(x!=0);
	}
}

# Crud Concessionaria | Dart

```dart

import 'dart:io';

void main() {

  List ListaCarros = [];

  while(true){
    print("\n[X]Olá, bem vindo ao Crud de Concessionaria!");
    print("[1]Cadastrar.");
    print("[2]Apresentar.");
    print("[3]Alterar.");
    print("[4]Excluir.");
    print("[5]Sair.");
    var VerificadorMenu = stdin.readLineSync();

    if(VerificadorMenu == "1"){
      print("\n[X]Opção de Cadastrar");

      print("[X]Digite o codigo do carro: ");
      var Codigo = stdin.readLineSync();

      print("[X]Digite o nome do carro: ");
      var Nome = stdin.readLineSync();

      print("[X]Digite o ano do carro: ");  
      var Ano = stdin.readLineSync();

      print("[X]Digite o tipo de combustivel do carro: ");
      var Combustivel = stdin.readLineSync();

      print("[X]Digite a configuração do carro: ");
      var Configuracao = stdin.readLineSync();

      print("[X]Digite a quantidade de lugares do carro: ");
      var Lugares = stdin.readLineSync();

      print("[X]Digite o tipo de tração do carro: ");
      var Tracao = stdin.readLineSync();

      var DadosCadastro = ("[ " + Codigo + " | " + Nome + " | " + Ano + " | " + Combustivel + " | " + Configuracao + " | " + Lugares + " | " + Tracao + " ]");

      ListaCarros.add(DadosCadastro);
      print("\n[X]Carro Cadastrado!");

    }

    else if(VerificadorMenu == "2"){
      print("\n[X]Opção de Apresentar");

      if(ListaCarros.length == 0){
        print("[X]Nenhum usuário registrado!");
      }

      else{
        for (int i = 0; i < ListaCarros.length; i++){
          var PegaIndex = i.toString();
          print("Carro " + PegaIndex + ": " + ListaCarros[i]);
        }
      }
    }

    else if(VerificadorMenu == "3"){
      print("\n[X]Opção de Alterar");

      if(ListaCarros.length == 0){
        print("[X]Nenhum usuário registrado!");
      }

      else{
        print("[X]Digite o carro a ser alterado: ");
        var CarroAlterar = stdin.readLineSync();

        var VerificaContador = 0;

        for (int i = 0; i < ListaCarros.length; i++){
          var PegaIndex = i.toString();

          if(CarroAlterar == PegaIndex){
            VerificaContador = VerificaContador + 1;
          }

          else{
            VerificaContador = VerificaContador + 0;
          }
        }

        if(VerificaContador > 0){
          
          print("[X]Digite o codigo do carro: ");
          var Codigo = stdin.readLineSync();

          print("[X]Digite o nome do carro: ");
          var Nome = stdin.readLineSync();

          print("[X]Digite o ano do carro: ");  
          var Ano = stdin.readLineSync();

          print("[X]Digite o tipo de combustivel do carro: ");
          var Combustivel = stdin.readLineSync();

          print("[X]Digite a configuração do carro: ");
          var Configuracao = stdin.readLineSync();

          print("[X]Digite a quantidade de lugares do carro: ");
          var Lugares = stdin.readLineSync();

          print("[X]Digite o tipo de tração do carro: ");
          var Tracao = stdin.readLineSync();

          var DadosCadastro = ("[ " + Codigo + " | " + Nome + " | " + Ano + " | " + Combustivel + " | " + Configuracao + " | " + Lugares + " | " + Tracao + " ]");

          ListaCarros[int.parse(CarroAlterar)] = DadosCadastro;
          print("\n[X]Carro Alterado!");

        }

        else{
          print("\n[X]Carro inexistente");
        }
      }
    }

    else if(VerificadorMenu == "4"){
      print("\n[X]Opção de Excluir");

      if(ListaCarros.length == 0){
        print("[X]Nenhum usuário registrado!");
      }

      else{
        print("[X]Digite o carro a ser excluido: ");
        var CarroExcluir = stdin.readLineSync();

        var VerificaContador = 0;

        for (int i = 0; i < ListaCarros.length; i++){
          var PegaIndex = i.toString();

          if(CarroExcluir == PegaIndex){
            VerificaContador = VerificaContador + 1;
          }

          else{
            VerificaContador = VerificaContador + 0;
          }
        }

        if(VerificaContador > 0){
          ListaCarros.removeAt(int.parse(CarroExcluir));
          print("\n[X]Carro Removido!");
        }

        else{
          print("\n[X]Carro inexistente");
        }
      }
    }

    else if(VerificadorMenu == "5"){
      print("\n[X]Opção de Sair. Obrigado!");
      exit(0);
    }

    else {
      print("[X]Escolha uma opção válida!");
    }
  }
}

```

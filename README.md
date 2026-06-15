O MauiAppHotel é uma aplicação desenvolvida em .NET MAUI que simula o processo de reserva de hospedagem em um hotel. O sistema conduz o usuário por um fluxo completo de contratação, permitindo a seleção de suítes, definição do período da estadia, autenticação de usuários e gerenciamento de sessão.

O projeto foi desenvolvido com foco na integração entre múltiplas telas, compartilhamento de dados e armazenamento seguro de informações do usuário.

# Funcionamento

A aplicação é composta por diversas telas que representam as etapas de contratação da hospedagem.

Contratação de Hospedagem

Na tela inicial, denominada ContratacaoHospedagem, o usuário informa os dados necessários para a reserva.

Entre as opções disponíveis estão:

Escolha do tipo de suíte (Super Luxo, Luxo ou Simples);
Definição da quantidade de adultos;
Definição da quantidade de crianças;
Seleção das datas de check-in e check-out.

Para facilitar a interação, foram utilizados componentes como Picker, Stepper e DatePicker. Além disso, o sistema realiza validações para impedir que o usuário selecione períodos de hospedagem inválidos.

Após o preenchimento das informações, o botão "Calcular Valor" executa os cálculos necessários e encaminha o usuário para a próxima etapa.

Resumo da Hospedagem

A tela HospedagemContratada apresenta um resumo completo da contratação realizada.

Nela são exibidas informações como:

Tipo de suíte selecionada;
Quantidade de hóspedes;
Datas de entrada e saída;
Quantidade total de diárias;
Valor total da hospedagem.

Caso necessário, o usuário pode retornar à etapa anterior para modificar os dados informados ou prosseguir para a autenticação no sistema.

Login

Para acessar os recursos da aplicação, o usuário deve realizar o login informando seu endereço de e-mail e senha.

Caso ainda não possua uma conta cadastrada, existe a opção "Criar Cadastro", que direciona o usuário para a tela de registro.

Cadastro de Usuário

A tela CadastroUsuario permite o registro de novos usuários através do preenchimento de um formulário contendo:

Nome;
E-mail;
Senha.

Durante o processo de cadastro, o sistema verifica se o endereço de e-mail informado já está associado a outro usuário, evitando registros duplicados.

Após a conclusão do cadastro, o usuário é redirecionado para a tela de login para realizar sua autenticação.

Gerenciamento de Sessão

Uma vez autenticado, o usuário permanece conectado mesmo após o fechamento da aplicação. Esse comportamento é possível graças à utilização do SecureStorage, recurso responsável pelo armazenamento seguro das informações de sessão.

Também foi implementada a funcionalidade de logout, que remove os dados armazenados e encerra a sessão ativa do usuário.

# Conceitos Aplicados 

Durante o desenvolvimento deste projeto foram utilizados os seguintes conceitos:

Desenvolvimento de aplicações móveis multiplataforma com .NET MAUI;
Navegação entre múltiplas páginas;
Compartilhamento de dados utilizando BindingContext;
Utilização de controles como Picker, Stepper, DatePicker, Entry e Button;
Implementação de validações em formulários;
Cálculo de valores baseado em regras de negócio;
Manipulação de dados entre diferentes telas da aplicação;
Implementação de autenticação de usuários;
Gerenciamento de sessão utilizando armazenamento seguro;
Utilização do SecureStorage para persistência de informações sensíveis.

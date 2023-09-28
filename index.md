# Sistema de feedback contextualizado para chatbots

## Sumário
1. Introdução
2. Solução proposta
3. Conclusão
4. Referências


## Introdução

É muito comum hoje ver as pessoas comentando que seus modelos de Machine Learning não estão aprendendo corretamento com novos dados, o que é um problema muito conhecido, chamado de aprendizagem contínua. As AIs tem muita dificuldade de aprender com novos dados e guardar as informações que já eram conhecidas, sendo assim, estas acabam sendo esquecidas. Considerando esse problema, foi criado o conceito de  "Continual Knowledge Learning (CKL)", que consiste na capacidade do modelo de aprender continuamente novos conhecimentos enquanto atualiza informações sobre os antigos. Por outro lado, esse conceito também apresenta muitos desafios, como a adaptação dinâmica, ou seja, os modelos ainda possuem dificuldade para se adaptar a mudanças no ambiente e no contexto ao longo do tempo, o que é essencial para uma CKL eficaz, o esqueciemnto catastrófico, mesmo que seja uma de suas principais funções, ainda é um desafio para o CKL e, por último, a gestão de memória, uma vez que ainda é difícil desenvolver mecanismos eficazes para armazenar e recuperar informações relevantes de maneira eficiente. Ainda assim, é de grande importânacia que os modelos de Machine Learning sejam atualizados com a entrada de novos dados, para que ele não fique enviesado com dados do passado (concept drift). O objetivo é implementar uma forma de aprendizagem contínua no projeto que estou fazendo atualmente de reconhecimento de voz com AI para a IBM.


## Solução proposta 

**Contexto**: o projeto é composto por um Chatbot que tem o objetivo de entregar respostas rápidas ao usuário. Essas respostas serão baseadas em pesquisas da internet, e vão conter links e gráficos.

Considerando o contexto acima, é extremamente importante que a plataforma tenha uma sessão de feedbacks, para que o usuário possa dizer à aplicação se a resposta dada foi relevante ou não. Abaixo é possível visualizar o diagrama dessa solução.

<p align="center">
	<img width="70%" align="center" src="https://imgur.com/JjWSYvz.png"/>
</p>

Como é possível perceber, a minha proposta de solução é cíclica, mas iniciarei a explicação pelo bloco "Chatbot". Esse primeiro bloco representa toda a minha aplicação, desde o login até o chat e comunicação com o usuário em si. Ao usar a plataforma, o usuário fará perguntas relacionadas ao seu trabalho, e receberá respostas da internet em forma de texto, links e gráficos. Considerando a utilização da plataforma, as respostas dadas pelo chatbot precisam atender ao máximo as expectativas do usuário, e por isso foi criada uma sessão de feedbacks. Com isso, o usuário poderá dizer à plataforma se a resposta que ele recebeu foi relevante e se respondeu a pergunta feita.

Conforme a plataforma receber tais avaliações, ela vai enviá-las para o próximo bloco, o "Armazenamento de feedbacks", que vai guardar tudo que chega nele e posteriormente enviar para o próximo bloco, o de "Treinamento". Nessa parte, haverá um sistema que vai receber todos os feedbacks e com ele, avaliar como a plataforma está performando. Por exemplo, se muitos usuários deram negativo para uma certa resposta, significa que o algoritmo precisa entender o que tem de errado com ela, se é o conteúdo ou a qualidade, para melhorar e não cometer o mesmo erro novamente.

Feito todo esse treinamento, as novas informações são enviadas novamente para o chatbot, mas sendo necessário recarregar o atualizar o dataset já existente, para que ele passe a performar já com os dados atualizados.


## Conclusão

Portanto, é possível concluir que a solução acima é de extrema importância para a minha aplicação atual, e que implementá-la aumentará  o valor do produto final, já que ela vai permitir que a inteligência artificial tenha uma aprendizagem contínua. Na minha opnião, eu acho que a solução é viável, mas que terá problemas em sua implementação, uma vez que foi abordado na introdução desse artigo que modelos CKL ainda possuem muitos desafios. Por outro lado, acho que a parte de desenvolvimento do sistema de armazenamento de feedbacks e de treinamento dos mesmos não seja algo que demande muito tempo e dificuldade. Ademais, para fazer tal implementação na minha aplicação, seria necessário modificar o frontend em alguns detalhes, o que não é um problema, além de modificar o backend para receber os feedbacks, e também a arquitetura, para que seja possível conectar os sistemas já existentes com o de treinamento e armazenamento das avaliações.


## Referências

JANG, J. et al. **TOWARDS CONTINUAL KNOWLEDGE LEARNING OF LANGUAGE MODELS**. [s.l: s.n.]. Disponível em: <https://arxiv.org/pdf/2110.03215.pdf>. Acesso em: 28 set. 2023.
‌

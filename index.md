# Sistema de gestão de memória para Chatbots

## Sumário
1. Introdução
2. Solução proposta
3. Conclusão
4. Referências

## Introdução

É muito comum hoje ver as pessoas comentando que seus modelos de Machine Learning não estão aprendendo corretamento com novos dados, o que é um problema muito conhecido, chamado de aprendizagem contínua. As AIs tem muita dificuldade de aprender com novos dados e guardar as informações que já eram conhecidas, sendo assim, estas acabam sendo esquecidas. Considerando esse problema, foi criado o conceito de  "Continual Knowledge Learning (CKL)", que consiste na capacidade do modelo de aprender continuamente novos conhecimentos enquanto atualiza informações sobre os antigos. Por outro lado, esse conceito também apresenta muitos desafios, como a adaptação dinâmica, ou seja, os modelos ainda possuem dificuldade para se adaptar a mudanças no ambiente e no contexto ao longo do tempo, o que é essencial para uma CKL eficaz, o esqueciemnto catastrófico, mesmo que seja uma de suas principais funções, ainda é um desafio para o CKL e, por último, a gestão de memória, uma vez que ainda é difícil desenvolver mecanismos eficazes para armazenar e recuperar informações relevantes de maneira eficiente. Ainda assim, é de grande importânacia que os modelos de Machine Learning sejam atualizados com a entrada de novos dados, para que ele não fique enviesado com dados do passado (concept drift).

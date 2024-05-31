# Qual-o-seu-WhatsApp

Vamos adaptar o código para Ruby, mantendo a mesma lógica de validação de números de WhatsApp brasileiros com expressões regulares.

```ruby
def capturar_numero_whatsapp
  puts "Digite o número de telefone (com DDD):"
  numero = gets.chomp
  return numero
end

def validar_numero_whatsapp(numero)
  padrao = /^\(\d{2}\) 9 \d{4}-\d{4}$/
  if numero.match(padrao)
    true
  else
    false
  end
end

def main
  numero = capturar_numero_whatsapp
  if validar_numero_whatsapp(numero)
    puts "Número válido! Seu WhatsApp é: #{numero}"
  else
    puts "Número inválido. Verifique o formato (99) 9 9999-9999."
  end
end

main if __FILE__ == $0
```

## Explicação do Código em Ruby

- `capturar_numero_whatsapp`: Esta função solicita ao usuário que digite o número de telefone e o armazena na variável `numero`.
- `validar_numero_whatsapp`: Esta função utiliza a expressão regular armazenada na variável `padrao` para verificar se o número digitado segue o padrão brasileiro de WhatsApp.
- `main`: Esta é a função principal que chama as outras funções e exibe a mensagem apropriada baseada na validação do número.

Para executar este código, salve-o em um arquivo `.rb` e execute-o em um ambiente que suporte Ruby. Quando solicitado, digite o número de telefone para verificação.

Aqui está um exemplo completo de um script em Ruby que captura um número de telefone, verifica se ele segue o formato de um número de WhatsApp brasileiro usando expressões regulares e imprime uma mensagem com o resultado da validação:

```ruby
# Script para validar números de WhatsApp brasileiros

# Função para capturar o número de telefone do usuário
def capturar_numero_whatsapp
  puts "Digite o número de telefone (com DDD):"
  numero = gets.chomp
  return numero
end

# Função para validar o número de telefone usando expressões regulares
def validar_numero_whatsapp(numero)
  padrao = /^\(\d{2}\) 9 \d{4}-\d{4}$/
  if numero.match(padrao)
    true
  else
    false
  end
end

# Função principal que executa o script
def main
  numero = capturar_numero_whatsapp
  if validar_numero_whatsapp(numero)
    puts "Número válido! Seu WhatsApp é: #{numero}"
  else
    puts "Número inválido. Verifique o formato (99) 9 9999-9999."
  end
end

# Chama a função principal se o script for o arquivo principal executado
main if __FILE__ == $0
```

Para executar este script, salve-o em um arquivo com a extensão `.rb` e execute-o em um terminal ou ambiente de desenvolvimento que suporte Ruby. O script solicitará que você digite o número de telefone e, em seguida, verificará se ele está no formato correto.

Espero que este exemplo seja útil para quem precisar realizar o projeto.

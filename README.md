# Projetos_ruby

new_game = "s"

while new_game == "s"
	puts "Advinhe o número que estou pensando entre 1 e 100:"
	meu_numero = gets.to_i

	pc_numero = Random.rand(99) + 1
  #puts pc_numero
  
	tentativas = 1

	while pc_numero != seu_numero
		puts "O número é maior que #{meu_numero}" if pc_numero > meu_numero
		puts "O número é menor que #{meu_numero}" if pc_numero < meu_numero

		tentativas += 1

		puts "Tente novamente: "
		meu_numero = gets.to_i
	end

	puts "Parabéns, o número era #{pc_numero}"
	puts "Você usou #{tentativas} tentativas"

	puts "Deseja jogar novamente? (s/n)"
	new_game = gets.chomp
end

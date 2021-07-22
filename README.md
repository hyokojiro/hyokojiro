from time import sleep
print('='*31, '\n    \033[33mLOJINHA DO HYOKOJIRO\033[m\n', '='*31)

mercado = int(input('quantos reais você comprou? R$'))
for c in range(1):
	print('\nescolha uma dessas opções: \n[ 1 ] pagar com cartão de credito \n[ 2 ] pagar a vista')
compras = int(input('qual opção? '))

if compras == 1:
	juro = int(input('''\nvocê quer parcelar?
[ 1 ] sim 
[ 2 ] não 
escolha uma dessas opcoes: '''))	

	if juro == 1:
		parcelaas = int(input(f'você pode parcelar de 1 a 12 vezes. \nquantas vezes voce quer parcelar? '))
		dividindo = mercado / parcelaas
		print('\033[31mPROCESSANDO...\033[m')
		sleep(2)
		print(f'você vai pagar {dividindo:.2f} por {parcelaas} meses, pela sua compra de R${mercado}')
	elif juro == 2:
		print(f'\nvocê pagou R${mercado} tudo de uma vez no cartão de credito. ')
		
elif compras == 2:
	print(f'\nvocê pagou R${mercado} a vista.')

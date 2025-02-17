import pandas as pd
import os

# Pasta onde estão os arquivos
pasta_arquivos = "endereço dos arquivos"

# Lista todos os arquivos .xlsx na pasta
arquivos = [f for f in os.listdir(pasta_arquivos) if f.endswith(".xlsx")]

# Lista para armazenar os DataFrames
dfs = []

# Lê cada arquivo e adiciona à lista
for arquivo in arquivos:
    caminho_completo = os.path.join(pasta_arquivos, arquivo)
    df = pd.read_excel(caminho_completo)
    dfs.append(df)

# Concatena todos os DataFrames
df_final = pd.concat(dfs, ignore_index=True)

# Salva em um novo arquivo
df_final.to_excel("resultado_unificado.xlsx", index=False)

print("Unificação concluída! Arquivo salvo como 'resultado_unificado.xlsx'")

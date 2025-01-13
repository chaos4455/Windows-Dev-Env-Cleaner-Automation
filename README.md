## 🧹 Limpeza Profunda do Windows e Ambiente de Dev 🚀

<div style="background-color: #e0f7fa; border-radius: 10px; padding: 15px;">

  <div style="display: flex; flex-wrap: wrap; justify-content: space-around;">

    <div style="flex: 1; min-width: 200px; margin: 10px; background-color: #c8e6c9; border-radius: 8px; padding: 10px; text-align: center;">
     <h4 style="margin-bottom: 5px;">🪟 Limpeza do Windows</h4>
     <p>
        <img src="https://img.shields.io/badge/Temp-🗑️-blueviolet" alt="Temp" style="margin: 2px;" />
        <img src="https://img.shields.io/badge/Prefetch-🧹-blue" alt="Prefetch" style="margin: 2px;" />
        <img src="https://img.shields.io/badge/LocalTemp-📁-blue" alt="LocalTemp" style="margin: 2px;" />
     </p>
      <p>
       <code>%SystemRoot%\Temp\*</code>, <code>%SystemRoot%\Prefetch\*</code>, <code>%LocalAppData%\Temp\*</code>
      </p>
    </div>


    <div style="flex: 1; min-width: 200px; margin: 10px; background-color: #c8e6c9; border-radius: 8px; padding: 10px; text-align: center;">
     <h4 style="margin-bottom: 5px;">👨‍💻 Ambiente de Desenvolvimento</h4>
       <p>
          <img src="https://img.shields.io/badge/VSCode--Cache-🚀-green" alt="VSCode Cache" style="margin: 2px;" />
          <img src="https://img.shields.io/badge/Python--Pip-🐍-green" alt="Python Pip" style="margin: 2px;" />
          <img src="https://img.shields.io/badge/Node--npm-📦-green" alt="Node npm" style="margin: 2px;" />
         <img src="https://img.shields.io/badge/Git--Cache-💾-green" alt="Git Cache" style="margin: 2px;" />
       </p>
        <p>
           <code>VS Code</code>, <code>pip</code>, <code>npm</code>, <code>yarn</code>, <code>Git</code>
        </p>
     </div>

    <div style="flex: 1; min-width: 200px; margin: 10px; background-color: #c8e6c9; border-radius: 8px; padding: 10px; text-align: center;">
     <h4 style="margin-bottom: 5px;">🧠 Machine Learning</h4>
      <p>
          <img src="https://img.shields.io/badge/HuggingFace-🤗-lightcoral" alt="HuggingFace" style="margin: 2px;" />
         <img src="https://img.shields.io/badge/TensorFlow-🐙-lightcoral" alt="TensorFlow" style="margin: 2px;" />
         <img src="https://img.shields.io/badge/Keras-🧠-lightcoral" alt="Keras" style="margin: 2px;" />
        <img src="https://img.shields.io/badge/PyTorch-🔥-lightcoral" alt="PyTorch" style="margin: 2px;" />
      <img src="https://img.shields.io/badge/conda-⚙️-lightcoral" alt="Conda" style="margin: 2px;" />
       </p>
        <p>
           <code>Hugging Face</code>, <code>TensorFlow</code>, <code>Keras</code>, <code>PyTorch</code>, <code>Conda</code>
        </p>
    </div>

    <div style="flex: 1; min-width: 200px; margin: 10px; background-color: #c8e6c9; border-radius: 8px; padding: 10px; text-align: center;">
       <h4 style="margin-bottom: 5px;">🔄 Atualizações e Sistema</h4>
        <p>
           <img src="https://img.shields.io/badge/Windows--Update-🔄-cornflowerblue" alt="Windows Update" style="margin: 2px;" />
            <img src="https://img.shields.io/badge/System--Cleanup-🧹-cornflowerblue" alt="System Cleanup" style="margin: 2px;" />
        </p>
        <p>
         <code>Windows Update</code>, <code>DISM</code>, <code>SFC</code>
        </p>
      </div>

  </div>
</div>

Este script foi criado por **Elias Andrade** ([@chaos4455](https://github.com/chaos4455)) para automatizar a limpeza de caches do Windows e do seu ambiente de desenvolvimento, incluindo ferramentas de Machine Learning. Utilize com cautela e certifique-se de entender cada comando antes de executar.

### ⚠️ Disclaimer Importante ⚠️

*   **Risco:** Este script realiza ações que podem apagar dados temporários e de cache. Embora geralmente seguro, use por sua conta e risco.
*   **Executar como Administrador:** Para funcionar corretamente, execute o script como administrador.
*   **Verificação:** Revise o script antes de executar, especialmente se você tiver dúvidas sobre algum comando.

### ⚙️ Como Utilizar

1.  Copie o código abaixo.
2.  Crie um novo arquivo com a extensão `.bat` (ex: `limpeza_windows.bat`).
3.  Cole o código no arquivo.
4.  Execute o arquivo `.bat` como administrador.

```batch
@echo off
echo Iniciando a limpeza de cache...

:: Limpeza do cache do Windows 🪟
echo :: Limpando cache do Windows...
DEL /S /Q /F "%SystemRoot%\Temp\*"
DEL /S /Q /F "%SystemRoot%\Prefetch\*"
DEL /S /Q /F "%LocalAppData%\Temp\*"

:: Limpeza de cache do Visual Studio Code 👨‍💻
echo :: Limpando cache do Visual Studio Code...
DEL /S /Q /F "%AppData%\Code\Cache\*"
DEL /S /Q /F "%AppData%\Code\CachedData\*"
DEL /S /Q /F "%AppData%\Code\GPUCache\*"
DEL /S /Q /F "%AppData%\Code\User\workspaceStorage\*"

:: Limpeza de cache do Python (pip) 🐍
echo :: Limpando cache do Python (pip)...
pip cache purge
DEL /S /Q /F "%LocalAppData%\pip\Cache\*"

:: Limpeza de cache do Node.js e npm 📦
echo :: Limpando cache do Node.js e npm...
npm cache clean --force
DEL /S /Q /F "%AppData%\npm-cache\*"

:: Limpeza de cache do yarn (se aplicável) 🧶
echo :: Limpando cache do yarn (se aplicável)...
yarn cache clean

:: Limpeza do cache global do Git 💾
echo :: Limpando cache do Git...
DEL /S /Q /F "%UserProfile%\.gitcache\*"

:: Limpeza do cache do Microsoft Store 🏪
echo :: Limpando cache da Microsoft Store...
DEL /S /Q /F "%LocalAppData%\Packages\Microsoft.WindowsStore_*\LocalCache\*"

:: Limpeza de cache de pacotes e modelos de Machine Learning 🧠

:: Limpeza de cache do Transformers (Hugging Face) 🤗
echo :: Limpando cache do Transformers (Hugging Face)...
DEL /S /Q /F "%UserProfile%\.cache\huggingface\*"

:: Limpeza de cache do TensorFlow 🐙
echo :: Limpando cache do TensorFlow...
DEL /S /Q /F "%UserProfile%\AppData\Local\Temp\.tensorflow\*"

:: Limpeza de cache do Keras 🧠
echo :: Limpando cache do Keras...
DEL /S /Q /F "%UserProfile%\.keras\datasets\*"
DEL /S /Q /F "%UserProfile%\.keras\models\*"

:: Limpeza de cache do PyTorch 🔥
echo :: Limpando cache do PyTorch...
DEL /S /Q /F "%UserProfile%\.cache\torch\*"
DEL /S /Q /F "%UserProfile%\.torch\*"

:: Limpeza do cache de modelos e pacotes de IA com pip e conda ⚙️
echo :: Limpando cache de modelos e pacotes de IA (pip/conda)...
pip cache purge
conda clean --all --yes

:: Limpeza do cache de atualizações do Windows 🔄
echo :: Limpando cache de atualizações do Windows...
net stop wuauserv
net stop bits
DEL /S /Q /F "%SystemRoot%\SoftwareDistribution\Download\*"
net start wuauserv
net start bits

:: Limpeza de arquivos temporários de atualizações do sistema 🧹
echo :: Realizando limpeza de arquivos temporários de atualizações do sistema...
DISM /Online /Cleanup-Image /StartComponentCleanup /ResetBase
sfc /scannow

echo Limpeza completa de cache de sistema, ferramentas de desenvolvimento e Machine Learning! ✔️
pause

```

📝 Explicação dos Comandos
DEL /S /Q /F: Comando para apagar arquivos.

/S: Apaga arquivos em subdiretórios.

/Q: Modo silencioso (sem confirmação).

/F: Força a remoção de arquivos somente leitura.

pip cache purge: Limpa o cache do pip (gerenciador de pacotes do Python).

npm cache clean --force: Limpa o cache do npm (gerenciador de pacotes do Node.js).

yarn cache clean: Limpa o cache do yarn (outro gerenciador de pacotes do Node.js).

conda clean --all --yes: Limpa o cache do conda (gerenciador de pacotes e ambientes do Anaconda).

net stop wuauserv: Para o serviço do Windows Update.

net stop bits: Para o serviço Background Intelligent Transfer Service (BITS).

net start wuauserv: Inicia o serviço do Windows Update.

net start bits: Inicia o serviço Background Intelligent Transfer Service (BITS).

DISM /Online /Cleanup-Image /StartComponentCleanup /ResetBase: Limpa componentes do sistema corrompidos.

sfc /scannow: Verifica e repara arquivos do sistema.

🎯 Contribuições
Sinta-se à vontade para contribuir com melhorias para este script através do meu repositório no GitHub: chaos4455

Espero que este script ajude a manter seu ambiente limpo e otimizado! 😄

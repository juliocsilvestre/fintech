# 💰 Fintech - React + TypeScript + Vite

Este projeto faz parte do **curso de React e TypeScript da Origamid** e consiste no desenvolvimento de uma aplicação Fintech utilizando **React, TypeScript e Vite**.

## 🚀 Tecnologias utilizadas

- **React** – Biblioteca para construção de interfaces modernas e dinâmicas
- **TypeScript** – Superset do JavaScript que adiciona tipagem estática
- **Vite** – Ferramenta de build rápida e otimizada
- **ESLint** – Linter para manter um código limpo e padronizado

## 📦 Configuração do projeto

Este template fornece uma configuração mínima para rodar **React com Vite** e **Hot Module Replacement (HMR)**, além de algumas regras do **ESLint**.

Atualmente, dois plugins oficiais estão disponíveis:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react) – Usa [Babel](https://babeljs.io/) para Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) – Usa [SWC](https://swc.rs/) para Fast Refresh

## 🔧 Expansão da configuração do ESLint

Se você está desenvolvendo um aplicativo para produção, é recomendável ativar regras de lint com reconhecimento de tipos:

```js
export default tseslint.config({
	extends: [
		...tseslint.configs.recommendedTypeChecked,
		...tseslint.configs.strictTypeChecked, // Para regras mais rigorosas
		...tseslint.configs.stylisticTypeChecked, // Para regras de estilo opcionais
	],
	languageOptions: {
		parserOptions: {
			project: ["./tsconfig.node.json", "./tsconfig.app.json"],
			tsconfigRootDir: import.meta.dirname,
		},
	},
});
```

### 📌 Plugins adicionais recomendados

Você pode instalar os seguintes plugins para aprimorar as regras do ESLint no React:

```bash
npm install eslint-plugin-react-x eslint-plugin-react-dom --save-dev
```

Adicione-os ao `eslint.config.js`:

```js
import reactX from "eslint-plugin-react-x";
import reactDom from "eslint-plugin-react-dom";

export default tseslint.config({
	plugins: {
		"react-x": reactX,
		"react-dom": reactDom,
	},
	rules: {
		...reactX.configs["recommended-typescript"].rules,
		...reactDom.configs.recommended.rules,
	},
});
```

## 🛠️ Como rodar o projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/juliocsilvestre/fintech.git
   cd fintech
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Rode o projeto localmente:
   ```bash
   npm run dev
   ```

## 📄 Licença

Este projeto é desenvolvido para fins educacionais no curso da **Origamid** e não possui uma licença específica.

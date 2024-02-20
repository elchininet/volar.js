# Volar.js

## Packages

```
@volar/language-core
  |
  |--- @volar/language-service
        |
        |--- @volar/language-server
        |     |
        |     |--- @volar/vscode (as a client to the language server)
        |
        |--- @volar/kit (encapsulates @volar/language-service for Node.js applications)
        |
        |--- @volar/monaco (integrates @volar/language-service into Monaco Editor)
```

### @volar/language-core

This module contains the core language processing functionalities, such as creating and updating virtual code objects. It serves as the foundation for the other modules, providing basic language processing capabilities.

### @volar/language-service

This module provides language service functionalities, such as offering IntelliSense features. It depends on `@volar/language-core` for obtaining and processing virtual code, and then provides corresponding language services.

### @volar/language-server

This module acts as a language server, utilizing the language services provided by `@volar/language-service` and offering these services to clients (like VS Code) through the Language Server Protocol (LSP). It also relies on `@volar/language-core` for handling basic language processing tasks.

### @volar/vscode

This module acts as a Language Server Protocol (LSP) language client. Its primary responsibility is to communicate with the `@volar/language-server` module (acting as an LSP server) and integrate the language services provided by the server into the VS Code editor. This architecture allows for the reuse of language services across different editors and IDEs, with the implementation of the corresponding LSP client. In this case, `@volar/vscode` is the LSP client implementation for VS Code.

### @volar/kit

`@volar/kit` is a module that encapsulates `@volar/language-service`. It provides a simplified interface for using Volar's diagnostic and formatting features within Node.js applications.

### @volar/monaco

This module is an extension of Volar.js for the Monaco Editor. It utilizes the language services provided by `@volar/language-service` and integrates these services into the Monaco Editor. This includes features like syntax highlighting, code completion, and definition jumping. Essentially, `@volar/monaco` serves as a bridge to bring Volar.js's language services into the Monaco Editor.

## Sponsors

<table>
	<tbody>
		<tr>
			<td align="center" colspan="6">
				<br><a href="https://stackblitz.com/"><img
						src="https://raw.githubusercontent.com/vuejs/language-tools/HEAD/.github/sponsors/StackBlitz.png"
						height="80" /></a>
				<br><a href="https://blog.stackblitz.com/posts/webcontainer-api-is-here/">WebContainer API is here.</a>
				<br>In 2021 <a href="https://blog.stackblitz.com/posts/introducing-webcontainers/">we announced
					WebContainers</a>, a novel WebAssembly-based operating system which enables Node.js to run entirely
				inside the browser. Over the last two years, millions of developers have used WebContainers each month
				as it powers, among others, the StackBlitz editor.
			</td>
		</tr>
		<tr>
			<td align="center" colspan="6"><b>Sponsors</b></td>
		</tr>
		<tr>
			<td align="center"><a href="https://www.prefect.io/"><img
						src="https://raw.githubusercontent.com/vuejs/language-tools/HEAD/.github/sponsors/prefect.svg"
						height="40" /></a></td>
			<td align="center" colspan="5">
				<a href="https://nuxt.com/"><img
						src="https://raw.githubusercontent.com/vuejs/language-tools/HEAD/.github/sponsors/nuxt.svg"
						height="60" /></a>
				<br>The Intuitive Vue Framework
			</td>
		</tr>
		<tr>
			<td align="center" colspan="5">
				<a href="https://vuejs.org/"><img
						src="https://raw.githubusercontent.com/vuejs/language-tools/HEAD/.github/sponsors/vue.png"
						height="80" /></a>
				<br>The Progressive JavaScript Framework
			</td>
			<td align="center"><a href="https://www.programmier.bar/"><img src="https://github.com/programmierbar.png"
						height="60" /></a></td>
		</tr>
		<tr>
			<td align="center"><a href="https://www.leniolabs.com/"><img src="https://github.com/leniolabs.png"
						height="60" /></a></td>
			<td align="center" colspan="5">
				Support us via
				<a href="https://github.com/sponsors/johnsoncodehk">GitHub Sponsors</a>
				or
				<a href="https://opencollective.com/volarjs">Open Collective</a>
			</td>
		</tr>
		<tr>
			<td></td>
			<td></td>
			<td></td>
			<td></td>
			<td></td>
			<td></td>
		</tr>
	</tbody>
</table>

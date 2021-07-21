# Generics em Java

<img src="./imgs/img2.png" height="400" width="650" >



# Lista

<p> Uma exemplo do generics em Java é a Lista, nela é possível evitar códigos redundantes, repetição. No entanto, a lista recebe dados de acordo com o tipo.  Na imagem acima, por exemplo, só será aceito dados que sejam do tipo String.</p><br/>

# Wildcards

## Declarando Aluno e passando na função generics

<ul>Lista<Aluno> minhaLista = new List<Aluno>();</ul>
<ul>imprimeLista(minhaLista);</ul>

## Funcao Generics

<ul>public void imprimeLista(<mark>List<?> lista</mark>){ </ul>
    <ul>for(<mark>Object obj : lista</mark>){ </ul>
        <ul>System.out.println(obj); </ul>
    <ul>}</ul>
<ul>}</ul>

# UpperBounded Wildcard

<ul>public void imprimeLista(<mark>List<? extends Pessoa> listaPessoas</mark>){ </ul>
    <ul>for(<mark>Pessoa p : listaPessoas</mark>){ </ul>
        <ul>System.out.println(p); </ul>
    <ul>}</ul>
<ul>}</ul>

<p> Só permite passara listas que são herdeiras de pessoas (extends Pessoa).</p>
 
# LowerBounded Wildcard

<ul>public void imprimeLista(<mark>List<? super Pessoa> listaPessoas</mark>){ </ul>
    <ul>for(<mark>Pessoa p : listaPessoas</mark>){ </ul>
        <ul>System.out.println(p); </ul>
    <ul>}</ul>
<ul>}</ul>

<p> Qualquer herdeiro da class Pessoa, ele não vai aceitar. Só vai aceitar da classe pessoa para cima.</p>

<p>e.g. "Pessoas extends Cidadaos".


# Convenção
<p>Criada para utilização de caracteres nos Wildcards.</p>

<ul><b>K</b> para "Key", e.g.: Map<<b>K</b>,V></ul>
<ul><b>V</b> para "value", e.g.: Map< K,<b>V</b>></ul>
<ul><b>E</b> para "Element", e.g.: List<<b>E</b>></ul>
<ul><b>T</b> para "Type", e.g.: Collections#addAll</ul>
<ul><b>?</b> Quando for genérico</ul>


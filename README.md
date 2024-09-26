## Set `<T>`<br>
• Representa um conjunto de elementos (similar ao da Álgebra)<br>
• Não admite repetições<br>
• Elementos não possuem posição<br>
• Acesso, inserção e remoção de elementos são rápidos<br> 
• Oferece operações eficientes de conjunto: interseção, união, diferença<br> 
• Principais implementações:<br> 
• `HashSet` - mais rápido (operações O(1) em tabela hash) e não ordenado<br> 
• `TreeSet` - mais lento (operações O(log(n)) em árvore rubro-negra) e ordenado pelo compareTo do objeto (ou Comparator)<br> 
• `LinkedHashSet` - velocidade intermediária e elementos na ordem em que são adicionados<br> 

### Alguns métodos importantes:<br>
• add(obj), remove(obj), contains(obj) - Baseado em equals e hashCode<br>
• Se equals e hashCode não existir, é usada comparação de ponteiros<br>
• clear()<br>
• size()<br>
• removeIf(predicate)<br>
• addAll(other) - união: adiciona no conjunto os elementos do outro conjunto, sem repetição<br>
• retainAll(other) - interseção: remove do conjunto os elementos não contidos em other<br>
• removeAll(other) - diferença: remove do conjunto os elementos contidos em other<br>

### Como as coleções Hash testam igualdade?<br>
• Se `hashCode` e `equals` estiverem implementados:<br>
  • Primeiro `hashCode`. Se der igual, usa `equals` para confirmar.<br>
  • Lembre-se: `String`, `Integer`, `Double`, etc. já possuem `equals` e `hashCode`<br>
• Se `hashCode` e `equals` **NÃO** estiverem implementados:<br>
  • Compara as referências (ponteiros) dos objetos.<br>


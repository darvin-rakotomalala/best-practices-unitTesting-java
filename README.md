## Bonnes pratiques test unitaire Java | Spring Boot
Dans ce repo, nous allons voir quelques-unes des meilleures pratiques pour les tests unitaires de code Java - Spring Boot.

*Notez que je suis toujours dans le processus d'apprentissage - probablement sans fin :)-*

### Qu'est-ce que les tests unitaires en Java ?
---
Le **test unitaire** est une technique permettant de tester des unités individuelles de code source pour s'assurer qu'elles fonctionnent 
comme souhaité. En d'autres termes, les tests unitaires sont utilisés pour s'assurer que les plus petites parties testables possibles 
d'une application sont testées pour s'assurer qu'elles fonctionnent correctement.

Voici quelques-unes des meilleures pratiques pour les tests unitaires de code Java :
- **Écrire des tests avant d'écrire du code**
- **Déterminez la couverture de votre code de test**
- **Gardez vos tests unitaires petits et ciblés**
- **Séparer les classes de test du code source principal** - ils sont développés, exécutés et maintenus séparément du code de production.
- **Convention de dénomination des packages** - Le package de la classe de test doit correspondre au package de la classe source dont l'unité de code source sera testée
- **Assurez-vous que vous écrivez chaque test indépendamment de tous les autres** - assurez-vous que tous les tests unitaires sont indépendants les uns des autres. Cela vous aidera à identifier la cause première et à tester correctement l'unité de logique.
- **Ne supposez pas l'ordre dans lequel les tests d'un scénario de test s'exécutent** - our modifier l'ordre d'exécution des tests, annotez simplement votre classe de test à l'aide de  @FixMethodOrder  et spécifiez l'un des  MethodSorters disponibles : `@FixMethodOrder(MethodSorters.NAME_ASCENDING)`
- **Couvrir un scénario spécifique unique dans un cas de test JUnit** - écrivez toujours un test unitaire pour tester un seul scénario spécifique.
- **Utiliser les méthodes d'assertion les plus appropriées** - Utilisez toujours des assertions appropriées pour vérifier les résultats attendus par rapport aux résultats réels.
- **Mettre les paramètres d'assertion dans le bon ordre** - L'ordre correct des paramètres garantit que les messages de JUnit sont exacts.
- **Utiliser les annotations `@BeforeEach` et `@AfterEach`** - Les méthodes annotées avec `@BeforeEach` et `@AfterEach` s'exécutent avant et après respectivement pour chaque méthode annotée avec @Test
- **Conventions de dénomination des tests JUnit** - Les noms de test doivent être perspicaces et les utilisateurs doivent comprendre le comportement et les attentes du test en jetant simplement un coup d'œil au nom lui-même.
  Par exemple - given/when/then format - BDD style :
	- **givenEmployeeObject_whenSaveEmployee_thenReturnSavedEmployee**
	- **givenEmployeesList_whenFindAll_thenReturnListOfEmployees**
	- **givenEmployeeObject_whenUpdateEmployee_thenReturnUpdatedEmployee**
- **Faux services/dépendances externes** - moquer des services externes et simplement tester la logique et l'exécution de notre code pour différents scénarios. Nous pouvons utiliser divers frameworks comme **Mockito** , **EasyMock** et **JMockit** pour se moquer de services externes.
- **Isoler les tests unitaires des dépendances externes** - Des exemples typiques de dépendances externes sont les bases de données, les services Web et d'autres composants logiciels sur lesquels repose votre code)
- **Mettre en œuvre l'automatisation des tests** - Avec un outil de build tel que Maven ou Gradle ou un serveur d'intégration continue peut faciliter l'exécution de vos tests unitaires)
- **Évitez de tester les détails d'Implementation** - Par exemple, si vous testez une méthode qui appelle une autre méthode, vous ne devez pas tester les détails de la façon dont la seconde méthode est implémentée; cela peut conduire à des tests fragiles et difficiles à entretenir.
- **Dépendances externes fictives** - Cela se fait souvent à l'aide de frameworks factices tels que Powermock, Mockito, etc.
- **Utiliser des assertions pour valider la sortie attendue pour les tests unitaires** - Les programmeurs doivent tirer parti des assertions appropriées pour vérifier si les résultats attendus et réels sont identiques
- **Fournir des noms significatifs aux méthodes de test** - Cela aide les développeurs à comprendre facilement l'intention de la méthode de test
- **Maintenir les tests unitaires à jour**
- **Créer des tests de code indépendants** - Gardez les tests unitaires dans leurs propres packages et loin du code de production. Il est recommandé de les éloigner de votre code source de production en général.
- **Archiver uniquement les tests unitaires qui ont réussi**

*Le respect de bonnes pratiques de codage, telles que l'utilisation de noms de variables et de commentaires significatifs, facilitera la compréhension et la maintenance de votre code Java. Cela vous facilitera la vie - et celle des autres développeurs - lors de l'écriture de tests unitaires pour votre code.*

*Bon apprentissage... Bon codage...*

Ressources utiles :
- [Best Practices for Unit Testing in Java](https://www.developer.com/java/best-practices-unit-testing-java/)
- [JUnit Framework Best Practices](https://www.javaguides.net/2018/08/junit-framework-best-practices.html)

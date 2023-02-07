# Object-Oriented Design Prep

## Approach

1. Handle Ambiguity
2. Define Core Objects
3. Analyze Relationships
4. Investigate Actions

## Design Patterns

### Singleton Class

```java
public class Restaurant {
    private static Restaurant instance = null;
    private Restaurant() {}
    public static Restaurant getInstance() {
        if (instance == null) {
            instance = new Restaurant();
        }
        return instance;
    }
}
```

### Factory Method

```java
public class CardGame {
    public static CardGame createCardGame(GameType type) {
        if (type == GameType.Poker) {
            return new PokerGame();
        } else if (type == GameType.BlackJack) {
            return new BlackJackGame();
        }
        return null;
    }
}
```
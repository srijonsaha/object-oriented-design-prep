# Object-Oriented Design Prep

## Approach

1. Clarify Requirements
2. Define API of System
3. Identify Key Objects
4. Identify Relationships Between Objects
5. Identify Operations Supported By Objects

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
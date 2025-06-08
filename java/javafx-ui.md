# JavaFX: UI Layout, Controls, Events, and Multiple Windows

This document summarizes the use of JavaFX in developing graphical user interfaces (GUIs), including layout management, controls, event handling, and creating multiple or modal windows.

---

## Stage and Scene

- **Stage**: The main window of a JavaFX application.
- **Scene**: The container for all graphical elements (nodes).

```java
Stage stage = new Stage();
Scene scene = new Scene(root, 400, 300);
stage.setScene(scene);
stage.show();
```

---

## Layout Managers

JavaFX provides various layout containers:

### VBox

- Aligns elements vertically.

```java
VBox layout = new VBox();
layout.getChildren().addAll(label, button);
```

### HBox

- Aligns elements horizontally.

```java
HBox layout = new HBox();
layout.getChildren().addAll(btn1, btn2);
```

### Pane

- A general-purpose container for placing nodes at exact positions.

---

## UI Controls

| Control      | Purpose                          |
|--------------|----------------------------------|
| `Label`      | Displays static text             |
| `Button`     | Executes an action when clicked  |
| `TextField`  | Accepts user input               |
| `ListView`   | Displays scrollable list items   |
| `TableView`  | Displays structured row/column data |

```java
Label label = new Label("Enter your name:");
TextField input = new TextField();
Button button = new Button("Submit");
```

---

## Event Handling

Events respond to user interactions.

```java
button.setOnAction(event -> {
    System.out.println("Button clicked");
});
```

### Counter Example

```java
int count = 0;
Label label = new Label("No clicks yet.");
Button button = new Button("Click");

button.setOnAction(e -> {
    count++;
    label.setText("Clicked " + count + " times.");
});
```

---

## Creating Multiple Windows

1. Create a new `Stage`
2. Design the UI using layout containers (VBox/HBox)
3. Set the scene to the new stage
4. Call `show()`

```java
Stage newWindow = new Stage();
VBox layout = new VBox(new Label("Hello from another window"));
Scene newScene = new Scene(layout, 200, 100);
newWindow.setScene(newScene);
newWindow.show();
```

---

## Modal Windows

- Prevents interaction with other windows until closed.
- Used for dialogs, alerts, or login screens.

```java
newWindow.initModality(Modality.APPLICATION_MODAL);
```

---

## TableView and ListView

### ListView

```java
ObservableList<String> items = FXCollections.observableArrayList("A", "B", "C");
ListView<String> listView = new ListView<>(items);
```

### TableView

```java
TableView<Person> table = new TableView<>();
TableColumn<Person, String> nameCol = new TableColumn<>("Name");
nameCol.setCellValueFactory(new PropertyValueFactory<>("name"));
table.getColumns().add(nameCol);
```

---

## Properties and Data Binding

JavaFX allows automatic UI updates using properties and bindings.

```java
IntegerProperty count = new SimpleIntegerProperty(0);
Label label = new Label();
label.textProperty().bind(count.asString("Count: %d"));
```

---

## MVC Architecture (Model-View-Controller)

- **Model**: Holds application data (e.g., `SimpleStringProperty`, `SimpleIntegerProperty`)
- **View**: Layout and display (e.g., `VBox`, `HBox`)
- **Controller**: Handles interaction logic (button events, model updates)

MVC separates logic and UI, making code more maintainable.

---

## JavaFX Animation and Graphics (Brief Preview)

- Use `PathTransition`, `Timeline` for animation.
- Use `Pane` for custom shapes (e.g., `Circle`, `Rectangle`).

```java
Circle circle = new Circle(200, 200, 50);
PathTransition pt = new PathTransition();
pt.setNode(circle);
pt.setPath(new Circle(200, 200, 100));
pt.setCycleCount(PathTransition.INDEFINITE);
pt.play();
```

---



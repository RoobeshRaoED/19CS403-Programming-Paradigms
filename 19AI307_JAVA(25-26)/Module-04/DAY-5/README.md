# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Create a class Note that stores a note content. Allow saving multiple versions and restoring a previous one. (Memento Pattern)

## AIM:

To implement the Memento Pattern that allows a Note object to save multiple versions of its content and restore any previous version.

## ALGORITHM :

1. Create a Note class (Originator) that holds content and can create and restore mementos.
2. Create a Memento class to store the note’s state (content).
3. Create a Caretaker class to keep a list of saved mementos (versions).
4. Allow saving the current note content as a new memento in the caretaker.
5. Allow restoring a chosen previous version by retrieving a memento and updating the note’s content.

## PROGRAM:

```

import java.util.*;

class Note {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }

    public NoteMemento save() {
        return new NoteMemento(content);
    }

    public void restore(NoteMemento m) {
        this.content = m.getSavedContent();
    }
}

class NoteMemento {
    private final String content;

    public NoteMemento(String content) {
        this.content = content;
    }

    public String getSavedContent() {
        return content;
    }
}

class NoteHistory {
    private List<NoteMemento> history = new ArrayList<>();

    public void saveVersion(Note note) {
        history.add(note.save());
    }

    public NoteMemento getVersion(int index) {
        return history.get(index);
    }
}

public class NoteManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Note note = new Note();
        NoteHistory history = new NoteHistory();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            note.setContent(content);
            history.saveVersion(note);
        }

        int version = sc.nextInt();
        sc.nextLine();

        note.restore(history.getVersion(version));
        System.out.println(note.getContent());

        sc.close();
    }
}

```

## OUTPUT:

![](4E.png)

## RESULT:

The program enables saving multiple note versions and restoring any previous content using the Memento pattern.

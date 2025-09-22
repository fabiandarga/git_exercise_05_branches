# Übungsaufgabe: Branches erstellen und mergen

Dieses Beispiel zeigt dir, wie du Branches erstellen kannst, um an verschiedenen Funktionen zu arbeiten, und wie du Änderungen aus diesen Branches in den Hauptbranch mergen kannst. Wiederhole diese Übung, um das Erstellen von Branches und das Mergen besser zu verstehen und zu üben.

## Schritt 1
Initialisiere ein neues Git-Repository und erstelle einen Hauptbranch:

```bash
mkdir exercise_05_branches
cd exercise_05_branches
git init
echo "Initial content" > main.txt
git add main.txt
git commit -m "Initial commit"
```

## Schritt 2
Erstelle einen neuen Branch mit Namen *feature1*:

```bash
git branch feature1
```

## Schritt 3
Wechsle zum Branch `feature1` und erstelle eine neue Datei:

```bash
git checkout feature1
echo "Feature 1 content" > feature1.txt
git add feature1.txt
git commit -m "Added feature 1"
```

## Schritt 4
Wechsel zurück zu `main` und erstelle von dort einen weiteren Branch:
  
**!Achtung ggf. heißt der Branch "master"**
  
```bash
git checkout main
git branch feature2
```

## Schritt 5
Wechsle zum Branch `feature2` und erstelle eine neue Datei:

```bash
git checkout feature2
echo "Feature 2 content" > feature2.txt
git add feature2.txt
git commit -m "Added feature 2"
```

## Schritt 6
Wechsle zurück zum Hauptbranch und füge Änderungen hinzu:

```bash
git checkout main
echo "Additional content in main" >> main.txt
git add main.txt
git commit -m "Updated main branch"
```

## Schritt 7
Merge die Änderungen aus `feature1` in den Hauptbranch:

```bash
git merge feature1
```

## Schritt 8
Merge die Änderungen aus `feature2` in den Hauptbranch:

```bash
git merge feature2
```

## Schritt 9
Überprüfe die Commit-Historie und den Zustand der Dateien:

```bash
git log --oneline --graph --all
ls
```

Fertig :)
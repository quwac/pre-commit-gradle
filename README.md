pre-commit-gradle
================

Some custom gradle hooks for pre-commit.

See also: https://github.com/pre-commit/pre-commit-hooks


### Using pre-commit-gradle with pre-commit

Add this to your `.pre-commit-config.yaml`

    -   repo: https://github.com/quwac/pre-commit-gradle
        rev: v0.3.0+1.1.0  # Use the ref you want to point at
        hooks:
        -   id: gradle-check
        # -   id: ...


### Hooks available

- `gradle-check` - Run gradle unit test tasks
    - Change working directory `args: ['--dir', 'path/to/working/dir']`.
    - Use gradlew (gradle wrapper) `args: ['-w', --wrapper]`.
    - Print output from gradle command `args: ['-o', --output]`.
- `gradle-build` - Run gradle build tasks
    - Change working directory `args: ['--dir', 'path/to/working/dir']`.
    - Use gradlew (gradle wrapper) `args: ['-w', --wrapper]`.
    - Print output from gradle command `args: ['-o', --output]`.
- `gradle-spotless` - Run gradle spotless tasks for java linting
    - Require spotless plugin: [github](https://github.com/diffplug/spotless/tree/master/plugin-gradle)
    - Change working directory `args: ['--dir', 'path/to/working/dir']`.
    - Use gradlew (gradle wrapper) `args: ['-w', --wrapper]`.
    - Print output from gradle command `args: ['-o', --output]`.
- `gradle-task` - Run any arbitrary gradle commands
    - Provide task name(s) to execute via arguments `args: ['clean build bootRun']`
    - Change working directory `args: ['--dir', 'path/to/working/dir']`.
    - Use gradlew (gradle wrapper) `args: ['-w', --wrapper]`.
    - Print output from gradle command `args: ['-o', --output]`.

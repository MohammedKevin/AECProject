# Horizono

## Stucture

Everything added by us is in the Assest folder. In the asset folder is a Deep space folder. In this folder you can find the DevKit for the DeepSpace of the Ars Electronica Center. Don't change it. Don't even touch it!

## How to pull repo

* create new folder
* new git repo: git init
* git remote add origin https://github.com/MohammedKevin420/AECProject.git
* pull everything from master( git pull origin master);

## How to implement new things

* pull everything from master( git pull origin master);
* create new feature branch and check it out( git checkout -b StoryId-Storyname , Example: 1-CreateGitRepo)
* make changed in this branch and try to make commits as often as possible ( git commit -m "Message")
* when everything works and there are no error( git push origin StoryId-Storyname)
* git checkout master
* git pull origin master
* git checkout Featurebranch
* merge master into current branch( git merge master)
* resolve all conflicts
* push all changes ( git push origin StoryId-Storyname)
* switch to master( git checkout master)
* merge feature to master ( git merge StoryId-Storyname)
* git add .
* git commit -m "message"
* git push origin master
    
## How to add your changes


* Open our project.
* Open the AECProject scene( Assets/Sccenes/AecProject)
* Open your Project
* Copy all needed scripts inside our project and sort them in the existing project structur
* Move everything that you created and need into a new game object and rename it to your theme example (Tracking)
* Drag this game object from the hirachy window to the project window
* This will create a Prefab
* Drag the Prefab to a temp folder in our project
* Move the prefab to your scene object or create a new scene game object with the same structur as the other ones if your scene was not created yet. 
* Right click the prefab and click on Unpack Prefab completely
* Check if the project debugs and all scripts are included in the game objects

## How to run your a scene

The Project is managed by a state machine. A state machine can run a state. Every scene gameobject has a corresponding scene state that implements IState. The State machine can run different states.


```csharp

    IState sceneX;
    void Start() {

        stateMachine = new StateMachine();
        scene1 = GameObject.Find("/ScenenOneState").GetComponent<SceneOneState>();
        sceneX = GameObject.Find("/SceneXState").GetComponent<SceneXState>();
        Debug.Log(scene1);
        stateMachine.ChangeState(sceneX); // Select what scene should run in your case szene X
        stateMachine.RunState();
    }
```

In this exmaple sceneX is the scene you want to start. Instead of sceneX use sceneTwo for example.

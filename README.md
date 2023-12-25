#include <stdbool.h>
#include <stdio.h>

typedef struct Project{
  bool completed;
  char *project_title;
  char *project_link;
  char *language_used;
} Project;

Project* create_project(char*, char*);
void set_complete(Project*);
void set_link(Project*, char*);

int main(){
  Project *projects[4];
  
  projects[0] = create_project("Python standard MNIST Convolutional Neural Network", "Python");
  set_link(projects[0], "https://github.com/a1exxd0/PythonConvolutional");
  set_complete(projects[0]);

  projects[1] = create_project("Creating a stack class in C", "C");
  set_link(projects[1], "[https://github.com/a1exxd0/PythonConvolutional](https://github.com/a1exxd0/CreateClassInC/tree/main/IntegerStack)");
  set_complete(projects[1]);

  projects[2] = create_project("C++ 2 category convolutional NN", "C++");
  projects[3] = create_project("C++ Multithreaded Server", "C++");
}

Project* create_project(char *project_title, char *language_used){
  Project* project = malloc(sizeof(Project));
  project->project_title = project_title;
  project->language_used = language_used;
  project->completed = false;
}

void set_complete(Project* project){
  project->=completed = true;
}

void set_link(Project* project, char *project_link){
  project->project_link = project_link;
}



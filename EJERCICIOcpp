#include <iostream>
#include <string>
#include <vector>
using namespace std;
// Interfaz IProyecto
class IProyecto {
public:
    virtual void crear() = 0;
    virtual void editar() = 0;
    virtual void eliminar() = 0;
};
// Implementación de la clase Proyecto
class Proyecto : public IProyecto {
private:
    string nombre;
    vector<string> tareas;
public:
    Proyecto(string nombre) : nombre(nombre) {}
    void crear() override {
        cout << "Creando proyecto: " << nombre << endl;
    }
    void editar() override {
        cout << "Editando proyecto: " << nombre << endl;
    }
    void eliminar() override {
        cout << "Eliminando proyecto: " << nombre << endl;
    }
    void agregarTarea(string tarea) {
        tareas.push_back(tarea);
    }
    void editarTarea(int indice, string nuevaTarea) {
        if (indice >= 0 && indice < tareas.size()) {
            tareas[indice] = nuevaTarea; // Asignación por valor
        } else {
            cout << "Índice inválido para editar tarea" << endl;
        }
    }
    void eliminarTarea(int indice) {
        if (indice >= 0 && indice < tareas.size()) {
            tareas.erase(tareas.begin() + indice);
        } else {
            cout << "Índice inválido para eliminar tarea" << endl;
        }
    }
};
// Interfaz IComentario
class IComentario {
public:
    virtual void agregar() = 0;
    virtual void editar() = 0;
    virtual void eliminar() = 0;
};
// Implementación de la clase Comentario
class Comentario : public IComentario {
private:
    string texto;
public:
    Comentario(string texto) : texto(texto) {}
    void agregar() override {
        cout << "Agregando comentario: " << texto << endl;
    }
    void editar() override {
        cout << "Editando comentario: " << texto << endl;
    }
    void eliminar() override {
        cout << "Eliminando comentario: " << texto << endl;
    }
};
// Interfaz IArchivo
class IArchivo {
public:
    virtual void subir() = 0;
    virtual void descargar() = 0;
    virtual void compartir() = 0;
};
// Implementación de la clase Archivo
class Archivo : public IArchivo {
private:
    string nombre;
    vector<char> contenido;
public:
    Archivo(string nombre) : nombre(nombre) {}
    void subir() override {
        cout << "Subiendo archivo: " << nombre << endl;
    }
    void descargar() override {
        cout << "Descargando archivo: " << nombre << endl;
    }
    void compartir() override {
        cout << "Compartiendo archivo: " << nombre << endl;
    }
    void agregarContenido(char dato) {
        contenido.push_back(dato);
    }
    void editarContenido(int indice, char nuevoDato) {
        if (indice >= 0 && indice < contenido.size()) {
            contenido[indice] = nuevoDato;
        } else {
            cout << "Índice inválido para editar contenido" << endl;
        }
    }
};
int main() {
  // Ejemplo de uso de las clases
  Proyecto proyecto1("Mi primer proyecto");
  proyecto1.crear();
  Comentario comentario1("Este es mi primer comentario");
  comentario1.agregar();
  Archivo archivo1("archivo.txt");
  archivo1.subir();
  return 0;
}

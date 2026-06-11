from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

todos = []

@app.route('/')
def index():
    return render_template('index.html', todos=todos)

@app.route('/add', methods=['POST'])
def add():
    todo_item = request.form.get('todo')
    if todo_item:
        todos.append(todo_item)
    return redirect(url_for('index'))

@app.route('/delete/<int:index_id>')
def delete(index_id):
    if 0 <= index_id < len(todos):
        todos.pop(index_id)
    return redirect(url_for('index'))

if __name__ == '__main__':
    app.run(debug=True)

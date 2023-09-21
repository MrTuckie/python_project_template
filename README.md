# python_project_template
project template for python projects

# Python

A intenção desse documento é auxiliar no gerenciamento do meu desenvolvimento com Python 3, além de entender e estruturar códigos no geral.

Se estiver perdido, comece por: [Roadmap.sh](https://roadmap.sh/python)

**[Triangle-headed Arrows with Bent Tips](https://www.cyberdefinitions.com/arrow-symbols.html)**

Conteúdos:

# 📁 Estrutura básica de todo código

Baseado nesse artigo aqui:

- [https://docs.python-guide.org/writing/structure/](https://docs.python-guide.org/writing/structure/)

```
project_name/
↳ docs/ # pasta para o sphinx construir a documentação
↳	logs/ # pasta para enventuais logs
↳	src/ # código fonte
			↳ __init__.py
			↳ classes/
				↳ __init__.py
↳	tests/ # código teste
↳	README.md
↳	requirements.txt
↳	.gitignore
↳	.env
↳	LICENSE

# opcionais
↳ data/ # pasta para guardar dados (csv,etc)
↳notebooks/ # notebooks para eventuais testes
↳ queries/ # arquivos de consulta no banco de dados
```

# 🧪 Estrutura dos testes

Use o pytest, de preferência

```
tests/
		↳__init__.py # por algum motivo, isso é necessário
		↳test_classes/
								↳ test_example.py	
		↳test_helpers/
								↳ test_example_2.py
```

Exemplo de código de teste `test_new_logger.py`

```python
from src.helpers import new_logger # importando a função
from datetime import datetime

class Test_new_logger():
    def test_now_time(self):
        r = new_logger.now_date_time_str(True)
        now = datetime.now().strftime("%d-%m-%y")
        assert r == now
```

# 🐍 Estilo do código

PEP8: [https://peps.python.org/pep-0008/](https://peps.python.org/pep-0008/)

[https://marketplace.visualstudio.com/items?itemName=ms-python.autopep8](https://marketplace.visualstudio.com/items?itemName=ms-python.autopep8)

[https://pypi.org/project/autopep8/](https://pypi.org/project/autopep8/)

# ⏲️ Medindo performance

Instead use “***perf_counter()***”. This will give you the most accurate way for calculating how much time taken by the code to run.

```python
from time import perf_counter
def checking_performance():
  start_time = perf_counter()
  time.sleep(1)
  end_time = perf_counter()
  print(end_time - start_time)
```

# python topics

## Best Practices

[[AI to improve your code](https://www.freecodecamp.org/news/how-to-use-ai-to-improve-code-quality/)](https://www.notion.so/AI-to-improve-your-code-ec92610490a94a95898523d13039eeed?pvs=21)

[Software Design Document Template](https://www.notion.so/Software-Design-Document-Template-5142c97ef5624695b41202b30a78368f?pvs=21)

### Documentation

- [https://docs.python-guide.org/writing/documentation/](https://docs.python-guide.org/writing/documentation/)

[[Code Diagnosis](https://www.arjancodes.com/diagnosis/3859481204?cid=b225c133-5715-4a83-b488-0f82ee4d0861) & Documentation](https://www.notion.so/Code-Diagnosis-Documentation-d063331228c14292927b3bedac8bff5e?pvs=21)

[SPHINX](https://www.notion.so/SPHINX-b5925b6284434d13b3e97abe93700373?pvs=21)

## OOP

[OOP](https://www.notion.so/OOP-e588742280894d94b5a8ca5befb2c1e7?pvs=21)

## Async

[Async](https://www.notion.so/Async-d733cfbfdbca43f0b5e7122d215d467a?pvs=21)

## Code Architecture

[**Factory Method**](https://www.notion.so/Factory-Method-9c488c68d5134ef58298a30e9d691d68?pvs=21)

[Dependency Inversion and Injection](https://www.notion.so/Dependency-Inversion-and-Injection-f71ec39942f8462d85f015447af499bf?pvs=21)

## Testing

[Unit Testing](https://www.notion.so/Unit-Testing-c388c85db0d94107b61a8a03aa2a2a33?pvs=21)

## CI/CD

## Random

[Django](https://www.notion.so/Django-8741c58db61343508fbb5ea49a4c084d?pvs=21)

### Materiais diversos

- [Playlist](https://www.youtube.com/watch?v=pxuXaaT1u3k&list=PLC0nd42SBTaMpVAAHCAifm5gN2zLk2MBo) do Aarjan codes

[Logs](https://www.notion.so/Logs-3649d0bb0e654ee8afe70d5eb06f930b?pvs=21)

[](https://www.notion.so/99b3b9adc17f4d0080e6e4d45a4a191a?pvs=21)
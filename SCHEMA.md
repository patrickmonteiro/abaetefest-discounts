# Schema — products.json

## Estrutura raiz

| Campo        | Tipo   | Descrição                              |
|-------------|--------|----------------------------------------|
| `updated_at` | string | ISO 8601 — quando foi atualizado       |
| `source`     | string | `"amazon"`                             |
| `products`   | array  | Lista de produtos                      |

## Produto

| Campo            | Tipo         | Obrigatório | Descrição                              |
|-----------------|--------------|-------------|----------------------------------------|
| `id`             | string       | ✅           | ID único (ex: ASIN da Amazon)          |
| `name`           | string       | ✅           | Nome do produto                        |
| `price`          | number       | ✅           | Preço atual em BRL                     |
| `original_price` | number\|null | ❌           | Preço original (para mostrar desconto) |
| `image`          | string       | ✅           | URL da imagem (direto da Amazon)       |
| `url`            | string       | ✅           | Link de afiliado (amzn.to/...)         |
| `category`       | string       | ✅           | Ver categorias abaixo                  |

## Categorias válidas

```
perfumes
saude_beleza
esportes_lazer
eletronicos
suplementos
livros
outros
```

## Ordem de exibição

Os produtos aparecem na ordem do array. Coloque os melhores primeiro.
Recomendado: perfumes e beleza no topo, outros no final.

# plantri
- run on https://cocalc.com/features/sage
```py
v1 = list(graphs.plantri_gen("4 -c1p"))
v2 = list(graphs.planar_graphs(4))

print([g.size() for g in v1]) # [6, 5, 4, 4, 3, 3]
print([g.size() for g in v2]) # [6, 5, 4, 4, 3, 3]
```

## signature
```py
# graphs.plantri_gen?
graphs.plantri_gen(self, options='', immutable=False)

# graphs.planar_graphs?
graphs.planar_graphs(
    self,
    order,
    minimum_degree=None,
    minimum_connectivity=None,
    exact_connectivity=False,
    minimum_edges=None,
    maximum_edges=None,
    maximum_face_size=None,
    only_bipartite=False,
    dual=False,
    immutable=False,
)
```

## memo
- `plantri_gen`에서 `planar_graphs`와 똑같은 결과 얻으려면 `-c1p` 붙여줘야 하는 듯
- sage의 plantri가 버전이 뭔지 모르겠음
  - 문서가 조금 다름
    - SageMath 10.7의 `graphs.plantri_gen?`
    - plantri 5.5 웹사이트의 manual
  - 두 사이트 모두 기본값이 `-m3`이라 써있는데 아닌것같음
    - `-p`랑 쓰면 `-m1`이 되나?
    - 이거 때문에 헷갈려서 시간 날림

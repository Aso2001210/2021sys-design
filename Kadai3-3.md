```uml
@startuml
start
if (今朝はご飯だった) then (Yes)
  :お昼はパンにしよう;
elseif (今朝はパンだった) then (Yes)
  :お昼はご飯にしよう;
else (No)
  :お昼は豪勢にしよう;
endif
stop
@enduml
```

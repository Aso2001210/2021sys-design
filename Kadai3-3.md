@startuml
start
if (今朝はご飯だった) then (yes)
  :お昼はパンにしよう;
elseif (今朝はパンだった) then (yes)
  :お昼はご飯にしよう;
else (no)
  :お昼は豪勢にしよう;
endif
stop
@enduml

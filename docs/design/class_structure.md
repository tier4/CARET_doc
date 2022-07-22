```plantuml

class Application {
}


class CallbackBase {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()

}
class Node {
}
class Publisher {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}
class Subscription {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}
class Executor {
}

class Timer {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}

class CallbackGroup {
}

class Communication {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}

class Path {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}

class NodePath {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}
class VariablePassing {
    + to_records()
    + to_dataframe()
    + to_timeseries()
    + to_histogram()
}


Application o-- Node
Application o-- Communication
Application o-- Path
Application o-- Executor
Path o-d- Communication
Path o-d- NodePath
Communication o-- Publisher
Communication o-- Subscription
Communication o-l- Node
Node o-- CallbackGroup
Node o-- VariablePassing
Node o-l- NodePath
NodePath o-- Publisher
NodePath o-- Subscription
NodePath o-- CallbackBase
CallbackGroup o-d- CallbackBase
CallbackBase o-d- Publisher
CallbackBase o-d- Timer
CallbackBase o-d- Subscription
Executor o-- CallbackGroup

```


# Beyond Design Patterns
> by: Anthony Ferrara  
> [http://joind.in/talk/view/13450][1]

* This talk is not *Design Patterns for Dummies*
* Gang-Of-Four Design Patterns Re-grouped

 | Creational | Structural | Behavioral
--- | --- | --- | ---
**Shim** | Abstract Factory,<br/>Object Pool,<br/>Prototype | Flyweight  | Iterator,<br/>Null Object
**Compositional** | Builder | Composite,<br/>Decorator,<br/>Façade,<br/>Proxy | Interpreter<br/>Mediator<br/>Observer
**Decompositional** | Factory Method | Bridge,<br/>Composite,<br/>Proxy | Chain of Responsibility,<br/>Command,<br/>Mediator,<br/>Memento,<br/>Observer,<br/>Strategy,<br/>Template Method

* Deduplicated Re-Groupings

 | Multiple Systems | Single Systems | Single Objects
--- | --- | --- | ---
**Information Flow?** | Mediator | Command | Observer
**Structure** | Adapter | Composite | Memento

* All Designs Patterns Do the Same Thing
	* **They Control Information Flow**
* What Is Information Flow?
	* `$msg` Message
	* `$obj` Logic
	* `$out = $obj->do($msg);`
	* `Ask` Is Always Stateful
	* `Tell` Is Always Stateful
	* `Translate` Can Be Stateless

 | Logic | Hybrid | Message
--- | --- | --- | ---
**Purpose** | Behaviour | General Code | State
**State** | Stateless | Stateful | Stateful
**Paradigm** | Functional | OOP? | Data

* Object Role Patterns
	* `Representer` e.g. `User`
	* `Doer` e.g. `EmailSystem`
	* `Dispatcher` e.g. `Controller`
	* `Translator` e.g. `UserView`
	* `Maker` e.g. `UserFactory`

 | State? | Logic? | Mode
--- | --- | --- | ---
**Representer** | User | No | Ask/Tell
**Doer** | No | Yes | Tell
**Dispatcher** | System | No | Translate
**Translator** | No | Yes | Translate
**Maker** | System | Yes | Ask

* Reading Material
	* *Practical Object-Oriented Design In Ruby*
	* [bit.ly/beyond-oop][2]
	* [bit.ly/oop-good-parts][3]
	* [bit.ly/18VsR1j][4]
	* Search for *"Message Passign OOP"*

[1]: http://joind.in/talk/view/13450
[2]: http://bit.ly/beyond-oop
[3]: http://bit.ly/oop-good-parts
[4]: http://bit.ly/18VsR1j
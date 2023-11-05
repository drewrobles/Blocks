# Blocks

Examples as blocks of code

### Deserializer
```
import com.google.gson.Gson
import org.junit.Assert.*
import org.junit.Test

class Person(val name: String) {}

class Deserializer {
    fun deserializePerson(serializedPerson: String): Person {
        return Gson().fromJson(serializedPerson, Person::class.java)
    }

    @Test
    fun testDeserializePerson() {
        var serializedPerson = "{\"name\":Drew}"
        var expectedPerson = Person("Drew")
        var actualPerson = deserializePerson(serializedPerson)
        assertEquals(expectedPerson.name, actualPerson.name)
    }
}
```


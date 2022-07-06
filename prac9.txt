<script>
    // Copying, passing, and comparing by value
    let x = 5
    let y = x
    x = 10
    console.log('Copying, passing, and comparing it by value. Output: ' + y)

    // Copying, passing, and comparing by reference
    x = {name: "Dev"}
    y = x
    x.name = "Dev1"
    console.log('Copying, passing, and comparing it by reference. Output: ' +      y.name)

    // References themselves are passed by value
    let count = 0
    const increase_count = (count) => {
        count++
    }
    increase_count(count)
    console.log('References get themselves passed by value. Output: ' + count)
    </script>

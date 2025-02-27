# Mekanism Asynchronous Database #

## What is this? ##
A simple and convenient tool for database management

### Using ###


Using the library is not difficult for basic tasks:

First you need to import the class itself using `from mekanism import Database`:

Let's look at using basic commands:

Recording data using `.set()`:

    # await db.set(key: str, *args)
    await db.set("your_key", "first_value", "second_value")


Receiving data using `.get()`:

    # await db.get(key: str, *args)
    await db.get("your_key", "first_value")
    returns "second_value"



Example:

    """   Conversation   """
    from mekanism import Database
    db = Database(db_name)
    
    async def main(db):
        username = input("Write your username: ")
        await asyncio.sleep(1)
        first_name = input("Write your first name: ")
        await asyncio.sleep(1)
        last_name = input("Write your last name: ")ы

        await db.set(username, [first_name, last_name])
        print(f"Hello, {(await db.get(username))[0]}")

    



## Developer ##
My profile: [DwZZd](https://github.com/DwZZd)
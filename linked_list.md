#Linked list 

    The purpose of a linked list is to be able to store information in a way that order matters. A linked list has a head, tail, and 
    nodes in between. To keep the list in order, we will point the node to the node directly before it and directly behind it, except in
    the cases of the head and tail that will only point to one node each. The big O notation for this data structure is O(n) because to 
    find a specific node, we loop through the linked list. 

    We can solve problems that require storing different information in memory, where you want to keep moving down the line of the 
    information, but you'd have to point in the direction it needs to go. Common errors that could occur for this data structure are not 
    removing or inserting a node correctly.



#Video
    https://www.youtube.com/watch?v=WwfhLC16bis&ab_channel=CSDojo


#Example:

    Let's say I have 3 children living at home. Names are:

    `Jameson,Calissa, and Kaden.`

    I want to keep these kids in order of oldest to youngest so I make a node called Jameson. Next is Calissa, so the data for the head of this linked list would be called Jameson and his node would point to Calissa by doing something like Jameson.next = Calissa. Then Calissa would point back to Jameson and forward to Kaden.

    Now, let's say I had another child named Brylee. I need to add her in last so now Kaden will point forward to her and Brylee will point back to Kaden. 

    `Jameson, Calissa, Kaden, and Brylee`

    Oh wow! Now I just adopted a little girl named Karah. She is older than Brylee and younger than Kaden, so she'll need to be pointing to both of them and Kaden will now point forward to Karah and Brylee will point back to Kaden. 

    Jameson, Calissa, Kaden, Karah, and Brylee`

    Jameson left to go on his mission, so he is no longer living at home. So Calissa is the new oldest and thus the new head of our linked
    list.

    `Calissa, Kaden, Karah, Brylee`



    Let's look at this linked list in diagram form:




    #Student Problem

    A family is trying to keep track of their streaming services and want to keep them in order of how much they cost a month.

    Make a linked list with the following services:

    Disney+
    Living Scriptures
    Netflix
    Hulu
    ESPN
 

    What!? The office isn't on Netfilx anymore? This family wants to switch out Netflix for Peacock.


```class Linked_List:
    def __init__(self):
        self.head = #Problem 1 what should the head be equal to to start?
        self.tail = None

    def insert_node_in_order(self, new_node):
        if self.head == None:
            self.head = new_node
            self.tail = new_node
        else:
            current = self.head
            while current.price <= new_node.price and current.next != None:
                current = current.next
            if current.prev != None:
                current.prev.next = new_node
                new_node.prev = current.prev
            else:
                self.head = new_node
            new_node.next = current
            current.prev = new_node

    def replace(self, old_value, new_value):
        """
        Searrch for all instances of 'old_value' and replace the value 
        to 'new_value'.
        """
        current = self.head

        if self.tail == self.head:
            self.head = new_value
            self.tail = new_value
        while current is not None:
            if current.name != old_value:
                current = current.next
            elif current.name == old_value:

            #Problem #2
                current.name = # Replace the old value with new value

    def print_self(self):
        current = self.head
        while current != None:
            print(current.name + ": $" + str(current.price))
            current = current.next
            

class Streaming_Service_Node:
    def __init__(self, name, price):
        self.name = name
        self.next = None
        self.prev = None
        self.price = price

linked_list = Linked_List()

netflix = Streaming_Service_Node("Netflix", 10.99)

#Problem #3
# insert netflix into the linked list

hulu = Streaming_Service_Node("Hulu", 7.99)
linked_list.insert_node_in_order(hulu)

disney = Streaming_Service_Node("Disney+", 8.99)
linked_list.insert_node_in_order(disney)

espn = Streaming_Service_Node("ESPN", 9.99)
linked_list.insert_node_in_order(espn)

ls = Streaming_Service_Node("Living Scriptures", 9.98)
linked_list.insert_node_in_order(ls)

print()
linked_list.print_self()
print()

peacock = Streaming_Service_Node("Peacock", 10.99)
linked_list.replace("Netflix", "Peacock")

print()
linked_list.print_self()
print()```






# practice-for-week-17-python-pipenv-setup-exercise
App Academy
Exercise: Pipenv Setup

In this short exercise, you will set up your first virtual environment using pipenv.

Setup
Create a new folder, representing a new project, in a directory of your choice. In this new project, create a new Python file that defines a class. Use the below class as a base. Feel free to add more methods or properties if you'd like.

class RegularPolygon:
    type = "Polygon"
    
    def __init__(self, num_sides, length):
        if num_sides < 3:
            raise Exception("A polygon must have at least 3 sides.")
        
        self.num_sides = num_sides
        self.length = length

    def identify_polygon(self):
        identifier_dict = {
            3: "Triangle",
            4: "Quadrilateral",
            5: "Pentagon",
            6: "Hexagon",
            7: "Heptagon",
            8: "Octagon",
            9: "Nonagon",
            10: "Decagon"
        }

        try:
            self.type = identifier_dict[self.num_sides]
        except KeyError:
            self.type = f"Polygon with {self.num_sides} sides"

    @classmethod
    def polygon_factory(cls, values):
        return [cls(num_sides, length) for num_sides, length in values]

    @staticmethod
    def get_perimeter(polygon):
        return polygon.num_sides * polygon.length
Creating the virtual environment
To create your environment, install pytest as your first dependency. This will create the Pipfile that will keep track of all the dependencies for your project. Feel free to install any other dependencies and use them within your code.

Using the environment
To use the virtual environment, you will need to enter the environment "shell". Try entering it and exiting. Notice that the dependencies you installed won't be usable unless your virtual environment shell is activated.

Keep this project handy as you'll be using it as the base for your next exercise!

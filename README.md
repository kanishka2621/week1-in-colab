{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyM4XynDdylMact15aLl4E+q",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/kanishka2621/Algorithm-to-swap-two-numbers-without-using-the-third-variable/blob/main/week1.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": 3,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "cXX9GuFabsCT",
        "outputId": "1a72993c-804b-40b8-e864-878e75e32726"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "enter number of units:560\n",
            "payable amount is:\n",
            "11000\n"
          ]
        }
      ],
      "source": [
        "def calculatebill(units):\n",
        "  if(units<=100):\n",
        "    return units*10;\n",
        "  elif(units<=200):\n",
        "    return((100*10)+(units-100)*15);\n",
        "  elif(units<=300):\n",
        "    return((100*10)+(units*15)+(units-200)*20);\n",
        "  elif(units>300):\n",
        "    return((100*10)+(100*15)+(100*20)+(units-300)*25);\n",
        "  return 0;\n",
        "units=int(input(\"enter number of units:\"))\n",
        "print(\"payable amount is:\")\n",
        "print(calculatebill(units));"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "def fact(n):\n",
        "  if n==1:\n",
        "    return 1\n",
        "  else:\n",
        "    return(n*fact(n-1))\n",
        "num=int(input(\"Enter a number:\"))\n",
        "result=fact(num)\n",
        "print(\"The factorial of\",num,\"is\",result)\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "XC6r3WN6cJc2",
        "outputId": "1c829e8b-32d5-4f01-eedf-426d1c05f52f"
      },
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter a number:12\n",
            "The factorial of 12 is 479001600\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "def tower_of_hanoi(disks,source,aux,target):\n",
        "  if (disks==1):\n",
        "    print(\"Move disk 1 from rod {} to rod {}.\".format(source,target))\n",
        "    return\n",
        "  tower_of_hanoi(disks-1,source,target,aux)\n",
        "  print(\"Move disk {} from rod {} to rod {}.\".format(disks,source,target))\n",
        "  tower_of_hanoi(disks-1,aux,source,target)\n",
        "disks=int(input(\"Enter the amount of disks:\"))\n",
        "tower_of_hanoi(disks,\"A\",\"B\",\"C\")\n",
        "\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "6dnNI0-tdo_u",
        "outputId": "a11b1238-ee2e-404a-c6bc-c201b17e49e1"
      },
      "execution_count": 9,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter the amount of disks:4\n",
            "Move disk 1 from rod A to rod B.\n",
            "Move disk 2 from rod A to rod C.\n",
            "Move disk 1 from rod B to rod C.\n",
            "Move disk 3 from rod A to rod B.\n",
            "Move disk 1 from rod C to rod A.\n",
            "Move disk 2 from rod C to rod B.\n",
            "Move disk 1 from rod A to rod B.\n",
            "Move disk 4 from rod A to rod C.\n",
            "Move disk 1 from rod B to rod C.\n",
            "Move disk 2 from rod B to rod A.\n",
            "Move disk 1 from rod C to rod A.\n",
            "Move disk 3 from rod B to rod C.\n",
            "Move disk 1 from rod A to rod B.\n",
            "Move disk 2 from rod A to rod C.\n",
            "Move disk 1 from rod B to rod C.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "class Cal:\n",
        "    def __init__(self, a, b):\n",
        "        self.a = a\n",
        "        self.b = b\n",
        "\n",
        "    def add(self):\n",
        "        return self.a + self.b\n",
        "\n",
        "    def mul(self):\n",
        "        return self.a * self.b\n",
        "\n",
        "    def div(self):\n",
        "        if self.b == 0:\n",
        "            return \"Cannot divide by zero\"\n",
        "        else:\n",
        "            return self.a / self.b\n",
        "\n",
        "    def sub(self):\n",
        "        return self.a - self.b\n",
        "\n",
        "a = int(input(\"Enter first number: \"))\n",
        "b = int(input(\"Enter second number: \"))\n",
        "obj = Cal(a, b)\n",
        "\n",
        "choice = 1\n",
        "while choice != 0:\n",
        "    print(\"0. Exit\")\n",
        "    print(\"1. Add\")\n",
        "    print(\"2. Subtraction\")\n",
        "    print(\"3. Multiplication\")\n",
        "    print(\"4. Division\")\n",
        "    choice = int(input(\"Enter choice: \"))\n",
        "\n",
        "    if choice == 1:\n",
        "        print(\"Result:\", obj.add())\n",
        "    elif choice == 2:\n",
        "        print(\"Result:\", obj.sub())\n",
        "    elif choice == 3:\n",
        "        print(\"Result:\", obj.mul())\n",
        "    elif choice == 4:\n",
        "        print(\"Result:\", round(obj.div(), 2))  # Corrected the calling of obj.div()\n",
        "    elif choice == 0:\n",
        "        print(\"Exiting\")\n",
        "    else:\n",
        "        print(\"Invalid choice\")\n",
        "\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "9C6BFiFbeKit",
        "outputId": "8d9f6148-31fa-4254-8972-23eada27ac77"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Enter first number: 12\n",
            "Enter second number: 6\n",
            "0. Exit\n",
            "1. Add\n",
            "2. Subtraction\n",
            "3. Multiplication\n",
            "4. Division\n",
            "Enter choice: 1\n",
            "Result: 18\n",
            "0. Exit\n",
            "1. Add\n",
            "2. Subtraction\n",
            "3. Multiplication\n",
            "4. Division\n",
            "Enter choice: 4\n",
            "Result: 2.0\n",
            "0. Exit\n",
            "1. Add\n",
            "2. Subtraction\n",
            "3. Multiplication\n",
            "4. Division\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [],
      "metadata": {
        "id": "K9tOfPfTf4Oh"
      },
      "execution_count": null,
      "outputs": []
    }
  ]
}

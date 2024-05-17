{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyNArJQBgrSBFAsusq2IOM4V",
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
        "<a href=\"https://colab.research.google.com/github/Yeswanthkotyada/octanet_may/blob/main/README.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "GCh3GZdLjrt3",
        "outputId": "a6e790e4-66f3-4aea-8da1-6b000ee16a80"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "Please insert your CARD\n",
            "Enter your Passsword: 5623\n",
            "Enter your atm pin: 5623\n",
            "\n",
            "      1==balance\n",
            "      2==withdraw balance\n",
            "      3==deposit balance\n",
            "      4==exit\n",
            "      \n",
            "Please enter your choice: 1\n",
            "Your current balance is 5500\n",
            "=======================================\n",
            "=======================================\n",
            "=======================================\n",
            "\n",
            "      1==balance\n",
            "      2==withdraw balance\n",
            "      3==deposit balance\n",
            "      4==exit\n",
            "      \n",
            "Please enter your choice: 3\n",
            "Please enter deposit_amount: 10000\n",
            "=======================================\n",
            "=======================================\n",
            "=======================================\n",
            "10000 is credited to your account\n",
            "=======================================\n",
            "=======================================\n",
            "Your updated balance is 15500\n",
            "=======================================\n",
            "=======================================\n",
            "\n",
            "      1==balance\n",
            "      2==withdraw balance\n",
            "      3==deposit balance\n",
            "      4==exit\n",
            "      \n",
            "Please enter your choice: 4\n"
          ]
        }
      ],
      "source": [
        "import time\n",
        "print(\"Please insert your CARD\")\n",
        "time.sleep(5)\n",
        "password=int(input(\"Enter your Passsword: \"))\n",
        "pin=int(input(\"Enter your atm pin: \"))\n",
        "balance=5500\n",
        "if pin==password:\n",
        "  while True:\n",
        "    print(\"\"\"\n",
        "      1==balance\n",
        "      2==withdraw balance\n",
        "      3==deposit balance\n",
        "      4==exit\n",
        "      \"\"\"\n",
        "      )\n",
        "    try:\n",
        "      option=int(input(\"Please enter your choice: \"))\n",
        "    except:\n",
        "      print(\"Please enter valid option\")\n",
        "\n",
        "    if option==1:\n",
        "      print(f\"Your current balance is {balance}\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "\n",
        "    if option==2:\n",
        "      withdraw_amount=int(input(\"Please enter withdraw_amount: \"))\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "      balance=balance-withdraw_amount\n",
        "      print(f\"{withdraw_amount} is debited from your account\")\n",
        "\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "\n",
        "      print(f\"Your current balance is {balance}\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "\n",
        "    if option==3:\n",
        "      deposit_amount=int(input(\"Please enter deposit_amount: \"))\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "\n",
        "      balance=balance+deposit_amount\n",
        "      print(f\"{deposit_amount} is credited to your account\")\n",
        "\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "      print(f\"Your updated balance is {balance}\")\n",
        "      print(\"=======================================\")\n",
        "      print(\"=======================================\")\n",
        "    if option==4:\n",
        "      break\n",
        "else:\n",
        "  print(\"Wrong pin Please try again\")"
      ]
    }
  ]
}
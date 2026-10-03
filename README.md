def create_frequency_table(items):
    table = {}

    for item in items:
        table[item] = table.get(item, 0) + 1

    return dict(sorted(table.items(), key=lambda pair: (-pair[1], pair[0])))


if __name__ == "__main__":
    values = ["python", "git", "python", "code", "git", "python"]

    print("Values:", values)
    print("Frequency table:", create_frequency_table(values))

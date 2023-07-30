def backspace_compare(s, t):
    def process_string(input_str):
        stack = []
        for char in input_str:
            if char == '#':
                if stack:
                    stack.pop()
            else:
                stack.append(char)
        return ''.join(stack)

    return process_string(s) == process_string(t)

# Test Example 1
s = "ab#c"
t = "ad#c"
print(backspace_compare(s, t))  # Output: True

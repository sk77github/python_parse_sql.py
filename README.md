# python_parse_sql.py
for parse sql statement with Python，like lex/yacc

output example:

 select b,z,a from cuishou where b = 'k' and z > 6 and y = 5 order by b,z
['SELECT', ['b', 'z', 'a'], 'FROM', 'cuishou', 'WHERE', ['b', '=', 'k'], 'AND', ['z', '>', '6'], 'AND', ['y', '=', '5'], 'ORDER', 'BY', ['b', 'z']]
- and1_expr: ['z', '>', '6']
- and2_expr: ['y', '=', '5']
- columns: ['b', 'z', 'a']
- order_by_terms: ['b', 'z']
- table: ['cuishou']
- where_expr: ['b', '=', 'k']
    
Expected "SELECT"

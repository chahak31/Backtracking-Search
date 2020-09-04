# Backtracking-Search
Search Algorithm used to solve Constraint Satisfaction Problems

    function BACKTRACK(assignment, csp): // csp is CONSTRAINT SATISFACTION PROBLEM 
      if assignment complete: return assignment
      var = SELECT-UNASSIGNED-VAR(assignment, csp)
      for value in DOMAIN-VALUES(var, assignment, csp):
        if value consistent with assignment:
          add {var = value} to assignment
          result = BACKTRACK(assignment, csp)
          if result != failure: return result
        remove {var = value} from assignment
       return failure
       

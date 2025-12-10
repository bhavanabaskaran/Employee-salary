# Employee-salary
def get_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    dept = input("Enter Department: ")
    basic = float(input("Enter Basic Salary: "))
    return name, emp_id, dept, basic
def calc_salary(basic):
    hra = basic * 0.20    
    da = basic * 0.10     
    pf = basic * 0.12      

    gross = basic + hra + da
    net = gross - pf

    return hra, da, pf, gross, net
def print_slip(name, emp_id, dept, basic, hra, da, pf, gross, net):
    
    print("\n============== EMPLOYEE SALARY SLIP ==============")
    print("Employee Name:", name)
    print("Employee ID  :", emp_id)
    print("Department:", dept)
    print("-----------------------------------------------")
    print("Basic Salary : Rs.", basic)
    print("HRA (20%) : Rs.", hra)
    print("DA (10%)  : Rs.", da)
    print("PF Deduction : Rs.", pf)
    print("-----------------------------------------------")
    print("Gross Salary : Rs.", gross)
    print("Net Salary    : Rs.", net)
    print("================================================")
    
name, emp_id, dept, basic = get_details()
hra, da, pf, gross, net = calc_salary(basic)
print_slip(name, emp_id, dept, basic, hra, da, pf, gross, net)

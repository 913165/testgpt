@startuml
class Employee {
  -id : Long
  -firstName : String
  -lastName : String
  -email : String
  -phone : String
  -address : String
  -birthDate : Date
  -gender : String
  -hireDate : Date
  -jobTitle : String
  -departmentId : Long
  -managerId : Long
  -salary : Double
  -active : boolean
  -terminationDate : Date
  -terminationReason : String
}

class Department {
  -id : Long
  -name : String
  -managerId : Long
}

class Job {
  -id : Long
  -title : String
  -description : String
  -salaryMin : Double
  -salaryMax : Double
}

class Training {
  -id : Long
  -name : String
  -description : String
  -startDate : Date
  -endDate : Date
  -employeeIds : List<Long>
}

class Payroll {
  -id : Long
  -employeeId : Long
  -payPeriodStartDate : Date
  -payPeriodEndDate : Date
  -grossPay : Double
  -taxes : Double
  -netPay : Double
}

class Performance {
  -id : Long
  -employeeId : Long
  -reviewDate : Date
  -reviewer : String
  -rating : int
  -comments : String
  -goals : List<String>
}

class Leave {
  -id : Long
  -employeeId : Long
  -leaveType : String
  -startDate : Date
  -endDate : Date
  -status : String
}

class Attendance {
  -id : Long
  -employeeId : Long
  -date : Date
  -clockInTime : Time
  -clockOutTime : Time
  -status : String
}

Employee -- Department : works in
Employee -- Employee : reports to
Employee -- Payroll : has payroll
Employee -- Performance : has performance review
Employee -- Attendance : has attendance record
Department -- Job : has job positions
Training -- Employee : required for training
Payroll -- Employee : paid to
Performance -- Employee : reviewed
Leave -- Employee : requested by
Attendance -- Employee : recorded for
@enduml

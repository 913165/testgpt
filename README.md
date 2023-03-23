```mermaid
graph TD;
  Employee((Employee)) -- works in --> Department((Department))
  Employee((Employee)) -- reports to --> Employee((Employee))
  Employee((Employee)) -- has payroll --> Payroll((Payroll))
  Employee((Employee)) -- has performance review --> Performance((Performance))
  Employee((Employee)) -- has attendance record --> Attendance((Attendance))
  Department((Department)) -- has job positions --> Job((Job))
  Training((Training)) -- required for --> Employee((Employee))
  Payroll((Payroll)) -- paid to --> Employee((Employee))
  Performance((Performance)) -- reviewed --> Employee((Employee))
  Leave((Leave)) -- requested by --> Employee((Employee))
  Attendance((Attendance)) -- recorded for --> Employee((Employee))

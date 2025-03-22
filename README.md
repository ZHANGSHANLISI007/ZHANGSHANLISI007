gantt
    title Facility Maintenance Project (PO:2026/1/1)
    dateFormat  YYYY-MM-DD
    axisFormat  %Y/%m/%d

    section Contract & Kickoff
    PO Release & Kickoff Meeting    :milestone, po, 2026-01-01, 0d
    Contract & PO Confirmation      :crit, contract_confirmation, after po, 2026-01-08, 7d

    section Personnel
    Recruitment                     :active, recruit, after po, 2026-01-08, 28d
    Training                        :training, after recruit, 2026-02-05, 14d
    Team Audit by Client            :audit_team, after training, 2026-02-19, 7d

    section Vehicles
    Vehicle Preparation             :vehicle_prep, after po, 2026-01-08, 21d
    Vehicle Modification            :vehicle_modify, after vehicle_prep, 2026-01-29, 7d
    Vehicle Inspection by Client    :crit, audit_vehicle, after vehicle_modify, 2026-02-05, 5d
    Vehicle Distribution            :vehicle_distribute, after audit_vehicle, 2026-02-10, 10d

    section Hub/Warehouse
    Site Selection                  :site_search, after po, 2026-01-08, 21d
    Contract Signing                :site_contract, after site_search, 2026-01-29, 14d
    Facility Inspection             :site_check, after site_contract, 2026-02-12, 7d

    section Tools & Equipment
    Tools Procurement               :tool_order, after po, 2026-01-08, 28d
    Tools Inspection by Client      :audit_tool, after tool_order, 2026-02-05, 10d
    Tools Distribution              :tool_distribute, after audit_tool, 2026-02-15, 14d

    section Final Delivery
    Project Acceptance              :milestone, deliver, 2026-03-05, 0d
    

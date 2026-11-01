import pypandoc

content = """# Day 1 — Introduction to ITSM

## What is ITSM?

IT Service Management (ITSM) is the way an organization connects people, processes, technology, and governance around IT services to create value.

ITSM is mainly about designing, delivering, supporting, and continuously improving IT services.

## Why does ITSM matter?

When an organization creates a product or service, there is a demand for it. The service needs to be designed, delivered to the customer, supported, and improved using customer feedback.

ITSM follows a similar approach for IT services. It helps provide a better experience for employees and customers and improves service quality.

The goal is not simply to close a ticket. The goal is to restore the service, reduce recurring disruptions, manage risk, and improve outcomes.

## IT, ITSM, and ITIL

- **IT:** The broader field of information technology, including technology and infrastructure.
- **ITSM:** The broader discipline of managing IT services and the processes around them.
- **ITIL:** A widely used framework that provides guidance and best practices for service management.

## ITSM lifecycle

1. **Demand:** Understand the need for a service.
2. **Design:** Design the service to meet that need.
3. **Deliver:** Make the service available to the customer.
4. **Support:** Help customers and employees when they need assistance.
5. **Improve:** Use feedback and experience to improve the service continuously.
"""

output_path = "/mnt/data/Day_1_Introduction_to_ITSM.md"
pypandoc.convert_text(content, "md", format="md", outputfile=output_path, extra_args=["--standalone"])
print(output_path)

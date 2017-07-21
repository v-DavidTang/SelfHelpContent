<properties
    pageTitle="VM performance is slow"
    description="VM 性能较低"
    authors="AlexKuriatnyk"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32411877"
    productPesIds="14749"
    cloudEnvironments="public"
    schemaVersion="1"
/>

# <a name="vm-performance"></a>VM 性能
---
{
    "resourceRequired": true,
    "title": "VM 性能问题",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "slow_vm_determination",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "如何确定虚拟机速度较慢？",
            "watermarkText": "选择选项",
            "dropdownOptions": [
                {
                    "value": "It's slower that it typically is",
                    "text": "它的速度比通常情况下慢"
                },
                {
                    "value": "Another virtual machine in the subscription is faster",
                    "text": "订阅中的另一个虚拟机速度更快"
                },
                {
                    "value": "Benchmarking tests not meeting minimum Azure specifications",
                    "text": "基准测试未满足 Azure 规范的最低要求"
                },
                {
                    "value": "It's faster in a non-Azure environment",
                    "text": "它在非 Azure 环境中速度更快"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_date",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "问题何时开始？",
            "required": false
        },
        {
            "id": "applications_on_vm",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "选择虚拟机上运行的应用程序",
            "dropdownOptions": [
                {
                    "value": "CRM Dynamics",
                    "text": "CRM Dynamics"
                },
                {
                    "value": "IIS / Web Front end",
                    "text": "IIS / Web 前端"
                },
                {
                    "value": "MySQL",
                    "text": "MySQL"
                },
                {
                    "value": "Oracle",
                    "text": "Oracle"
                },
                {
                    "value": "Remote Desktop Services",
                    "text": "远程桌面服务"
                },
                {
                    "value": "SAP Hanna",
                    "text": "SAP Hanna"
                },
                {
                    "value": "SharePoint",
                    "text": "SharePoint"
                },
                {
                    "value": "SQL",
                    "text": "SQL"
                },
                {
                    "value": "Other (describe below)",
                    "text": "其他"
                }
            ],
            "required": false
        },
        {
            "id": "additional_details",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "请提供这些详细信息",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "问题说明。"
                },
                {
                    "text": "你认为同一订阅中速度比这一较慢的虚拟机更快的虚拟机名称。"
                }
            ]
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json'>详细了解</a> IOPS（每秒输入/输出操作）的虚拟机规范和我们建议的基准测试工具"
        }
    ]
}
---


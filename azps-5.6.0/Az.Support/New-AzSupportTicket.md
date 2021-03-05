---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 0d86d4e01c39170975901f5c9262bc2857883eec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972433"
---
# <span data-ttu-id="b02bb-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b02bb-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="b02bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b02bb-103">Tworzy zgłoszenie do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-103">Creates a support ticket.</span></span>

## <span data-ttu-id="b02bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b02bb-104">SYNTAX</span></span>

### <span data-ttu-id="b02bb-105">CreateSupportTicketWithContactDetailParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b02bb-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02bb-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02bb-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02bb-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02bb-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02bb-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02bb-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02bb-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02bb-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02bb-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02bb-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02bb-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="b02bb-111">DESCRIPTION</span></span>
<span data-ttu-id="b02bb-112">Za pomocą tego polecenia cmdlet można utworzyć zgłoszenie do pomocy technicznej dotyczące problemów z rozliczeniami, zarządzaniem subskrypcją, przydziałem lub problemami technicznymi.</span><span class="sxs-lookup"><span data-stu-id="b02bb-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="b02bb-113">Użyj Get-AzSupportService i Get-AzSupportProblemClassification cmdlet, aby zidentyfikować usługę Azure i odpowiadające jej klasyfikacje problemów, dla których chcesz zażądać pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="b02bb-114">Należy określić następujące parametry:</span><span class="sxs-lookup"><span data-stu-id="b02bb-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="b02bb-115">Aby utworzyć obiekt CustomerContactDetail, New-AzSupportContactProfileObject polecenie cmdlet pomocnika.</span><span class="sxs-lookup"><span data-stu-id="b02bb-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="b02bb-116">Dostawcy rozwiązań w chmurze mogą utworzyć zgłoszenie do pomocy technicznej dla subskrypcji swoich klientów, logując się do dzierżawy swojego klienta i określając identyfikator dzierżawy głównej przy użyciu parametru *CSPHomeTenantId.*</span><span class="sxs-lookup"><span data-stu-id="b02bb-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="b02bb-117">__W przypadku biletów technicznych:__</span><span class="sxs-lookup"><span data-stu-id="b02bb-117">__For technical tickets:__</span></span>

<span data-ttu-id="b02bb-118">Aby określić nazwę zasobu, określ ARM identyfikator zasobu, używając *parametru TechnicalTicketResourceId.*</span><span class="sxs-lookup"><span data-stu-id="b02bb-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="b02bb-119">Zobacz przykład poniżej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-119">See an example below.</span></span> 

<span data-ttu-id="b02bb-120">__W przypadku biletów przydziału:__</span><span class="sxs-lookup"><span data-stu-id="b02bb-120">__For quota tickets:__</span></span>

<span data-ttu-id="b02bb-121">Aby zażądać zwiększenia przydziału dla operacji **Compute VM Cores,** **Batch,** **SQL Database** i SQL **Data Warehouse,** podaj dodatkowe szczegóły w obiekcie *QuotaTicketDetail.*</span><span class="sxs-lookup"><span data-stu-id="b02bb-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="b02bb-122">Obiekt QuotaTicketDetail ma 3 właściwości zgodnie z poniższym opisem.</span><span class="sxs-lookup"><span data-stu-id="b02bb-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="b02bb-123">Aby uzyskać szczegółową dokumentację, [kliknij tutaj.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="b02bb-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="b02bb-124">Aby uzyskać szczegółową dokumentację na temat konstruowania elementów ładowniczych dla różnych typów [przydziałów, kliknij tutaj](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="b02bb-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="b02bb-125">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b02bb-125">EXAMPLES</span></span>

### <span data-ttu-id="b02bb-126">Przykład 1. Utwórz bilet pomocy technicznej Do rozliczeń lub zarządzania subskrypcjami.</span><span class="sxs-lookup"><span data-stu-id="b02bb-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="b02bb-127">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów z rozliczeniami lub zarządzaniem subskrypcjami, dla których chcesz zażądać pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="b02bb-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-128">Przykład 2. Utwórz bilet pomocy technicznej dla zasobu Maszyny wirtualnej dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="b02bb-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="b02bb-129">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla maszyn wirtualnych dla klasyfikacji problemów systemu Windows, dla których chcesz zażądać pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="b02bb-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-130">Przykład 3. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla podstawowych maszyn wirtualnych dla określonej rodziny maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b02bb-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="b02bb-131">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID na klasyfikację problemów z obliczaniem przydziałów do podstawowych operacji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-132">Przykład 4. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla podstawowych zasobów o niskim priorytecie dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b02bb-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="b02bb-133">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów partii przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-134">Przykład 5. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału podstawowego maszyn wirtualnych dla określonej rodziny maszyny wirtualnej dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b02bb-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="b02bb-135">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów partii przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-136">Przykład 6. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału pul dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b02bb-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="b02bb-137">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów partii przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-138">Przykład 7. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału aktywnych zadań i harmonogramów zadań dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b02bb-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="b02bb-139">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów partii przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-140">Przykład 8. Tworzenie biletu obsługi przydziału w celu zwiększenia liczby kont wsadowych dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b02bb-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="b02bb-141">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów partii przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-142">Przykład 9. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla jednostek DTU dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b02bb-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="b02bb-143">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów z usługą Quota SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b02bb-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-144">Przykład 10. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla serwerów bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b02bb-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="b02bb-145">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów z usługą Quota SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b02bb-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-146">Przykład 11. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla jednostek DTU dla programu SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="b02bb-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="b02bb-147">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów programu SQL Date Warehouse przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-148">Przykład 12. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla serwerów usługi SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="b02bb-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="b02bb-149">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów programu SQL Data Warehouse przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-150">Przykład 13. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla podstawowych zasobów o niskim priorytecie dla usługi Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b02bb-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="b02bb-151">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów z usługą Quota Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b02bb-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-152">Przykład 14. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału podstawowych maszyn wirtualnych dla określonej rodziny maszyn wirtualnych dla usługi Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b02bb-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="b02bb-153">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemów z usługą Quota Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b02bb-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-154">Przykład 15. Tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla wystąpienia zarządzanego przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b02bb-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="b02bb-155">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać prawidłowe identyfikatory GUID dla klasyfikacji problemu usługi zarządzanego wystąpienia SQL przydziału.</span><span class="sxs-lookup"><span data-stu-id="b02bb-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-156">Przykład 16. Utwórz bilet pomocy technicznej, określając poszczególne parametry kontaktu klienta zamiast obiektu CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="b02bb-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-157">Przykład 17. Utwórz bilet pomocy technicznej z żądaniem odpowiedzi 24 x 7 z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b02bb-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b02bb-158">Przykład 18. Utwórz bilet pomocy technicznej w imieniu klienta, jeśli jesteś dostawcą rozwiązań w chmurze (CSP).</span><span class="sxs-lookup"><span data-stu-id="b02bb-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="b02bb-159">Program CSP powinien najpierw zalogować się do swojej dzierżawy, a następnie zalogować się do dzierżawy klienta, jak pokazano w poniższym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="b02bb-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="b02bb-160">Następnie muszą użyć parametru -CSPHomeTenantId, aby określić identyfikator dzierżawy głównej w momencie tworzenia biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="b02bb-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02bb-161">PARAMETERS</span></span>

### <span data-ttu-id="b02bb-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b02bb-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="b02bb-163">Dodatkowe adresy e-mail.</span><span class="sxs-lookup"><span data-stu-id="b02bb-163">Additional email addresses.</span></span>
<span data-ttu-id="b02bb-164">Wymienione tutaj adresy e-mail zostaną skopiowane w przypadku każdej korespondencji dotyczącej zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-165">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b02bb-165">-AsJob</span></span>
<span data-ttu-id="b02bb-166">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="b02bb-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="b02bb-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="b02bb-168">Jest to identyfikator dzierżawy głównej użytkownika dostawcy rozwiązań w chmurze, który próbuje utworzyć zgłoszenie do pomocy technicznej dla swojego klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="b02bb-169">-CustomerContactDetail</span></span>
<span data-ttu-id="b02bb-170">Dane kontaktowe klienta skojarzone z zasobem SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="b02bb-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="b02bb-171">-CustomerCountry</span></span>
<span data-ttu-id="b02bb-172">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-172">Customer country.</span></span>
<span data-ttu-id="b02bb-173">Ten kod musi być prawidłowym kodem iso Alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="b02bb-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="b02bb-174">-CustomerFirstName</span></span>
<span data-ttu-id="b02bb-175">Imię klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="b02bb-176">-CustomerLastName</span></span>
<span data-ttu-id="b02bb-177">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b02bb-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="b02bb-179">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-179">Customer phone number.</span></span>
<span data-ttu-id="b02bb-180">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="b02bb-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="b02bb-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="b02bb-182">Wywęszony język niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="b02bb-182">Peferred language of the custom.</span></span>
<span data-ttu-id="b02bb-183">Ten kod musi być prawidłowym kodem języka dla jednego z obsługiwanych języków wymienionych https://azure.microsoft.com/en-us/support/faq/ tutaj.</span><span class="sxs-lookup"><span data-stu-id="b02bb-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="b02bb-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="b02bb-185">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-185">Customer preferred time zone.</span></span>
<span data-ttu-id="b02bb-186">Musi to być prawidłowa System.TimeZoneInfo.Id wartości.</span><span class="sxs-lookup"><span data-stu-id="b02bb-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b02bb-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="b02bb-188">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="b02bb-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02bb-189">-DefaultProfile</span></span>
<span data-ttu-id="b02bb-190">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b02bb-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-191">— Opis</span><span class="sxs-lookup"><span data-stu-id="b02bb-191">-Description</span></span>
<span data-ttu-id="b02bb-192">Szczegółowy opis pytania lub problemu.</span><span class="sxs-lookup"><span data-stu-id="b02bb-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-193">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b02bb-193">-Name</span></span>
<span data-ttu-id="b02bb-194">Nazwa biletu pomocy technicznej, który tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02bb-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="b02bb-195">-PreferredContactMethod</span></span>
<span data-ttu-id="b02bb-196">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="b02bb-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="b02bb-197">-ProblemClassificationId</span></span>
<span data-ttu-id="b02bb-198">Każda usługa Azure ma własny zestaw kategorii problemów o nazwie klasyfikacja problemu odpowiadająca typowi problemu, który występuje.</span><span class="sxs-lookup"><span data-stu-id="b02bb-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="b02bb-199">Ten parametr jest identyfikatorem ARM zasobu ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="b02bb-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="b02bb-200">-ProblemStartTime</span></span>
<span data-ttu-id="b02bb-201">Data i godzina rozpoczęcia problemu.</span><span class="sxs-lookup"><span data-stu-id="b02bb-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="b02bb-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="b02bb-203">Dodatkowe szczegóły dotyczące biletu pomocy technicznej Przydział.</span><span class="sxs-lookup"><span data-stu-id="b02bb-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="b02bb-204">-Require24X7Response</span></span>
<span data-ttu-id="b02bb-205">Wskazuje, czy ten bilet pomocy technicznej wymaga odpowiedzi 24 godziny na 7 dni w tygodniu od platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b02bb-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-206">— Ważność</span><span class="sxs-lookup"><span data-stu-id="b02bb-206">-Severity</span></span>
<span data-ttu-id="b02bb-207">Ważność zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-207">Severity of the support ticket.</span></span>
<span data-ttu-id="b02bb-208">Wskazuje to na pilność sprawy, która z kolei określa czas reakcji zgodnie z umową o poziomie usług w ramach planu pomocy technicznej posiadanej z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b02bb-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="b02bb-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="b02bb-210">Jest to identyfikator zasobu usługi Azure (na przykład: zasób maszyn wirtualnych lub zasób usługi HDInsight), dla którego został utworzony bilet pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-211">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="b02bb-211">-Title</span></span>
<span data-ttu-id="b02bb-212">Tytuł zgłoszenia do pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="b02bb-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-213">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b02bb-213">-Confirm</span></span>
<span data-ttu-id="b02bb-214">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b02bb-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02bb-215">-WhatIf</span></span>
<span data-ttu-id="b02bb-216">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02bb-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02bb-217">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b02bb-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02bb-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02bb-218">CommonParameters</span></span>
<span data-ttu-id="b02bb-219">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02bb-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02bb-220">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b02bb-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02bb-221">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02bb-221">INPUTS</span></span>

### <span data-ttu-id="b02bb-222">Brak</span><span class="sxs-lookup"><span data-stu-id="b02bb-222">None</span></span>

## <span data-ttu-id="b02bb-223">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02bb-223">OUTPUTS</span></span>

### <span data-ttu-id="b02bb-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b02bb-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="b02bb-225">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b02bb-225">NOTES</span></span>

## <span data-ttu-id="b02bb-226">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b02bb-226">RELATED LINKS</span></span>

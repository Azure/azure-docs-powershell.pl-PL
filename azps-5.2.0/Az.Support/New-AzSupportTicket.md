---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335089"
---
# <span data-ttu-id="6816f-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6816f-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="6816f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6816f-102">SYNOPSIS</span></span>
<span data-ttu-id="6816f-103">Umożliwia utworzenie biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="6816f-103">Creates a support ticket.</span></span>

## <span data-ttu-id="6816f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6816f-104">SYNTAX</span></span>

### <span data-ttu-id="6816f-105">CreateSupportTicketWithContactDetailParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6816f-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6816f-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6816f-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6816f-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6816f-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6816f-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6816f-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6816f-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="6816f-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6816f-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="6816f-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6816f-111">Opis</span><span class="sxs-lookup"><span data-stu-id="6816f-111">DESCRIPTION</span></span>
<span data-ttu-id="6816f-112">Za pomocą tego polecenia cmdlet można utworzyć bilet pomocy technicznej na potrzeby rozliczeń, zarządzania abonamentami, przydziału lub problemów technicznych.</span><span class="sxs-lookup"><span data-stu-id="6816f-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="6816f-113">Za pomocą Get-AzSupportService i Get-AzSupportProblemClassification poleceń cmdlet można identyfikować usługę Azure, a odpowiadające im klasyfikacje problemów, dla których chcesz uzyskać pomoc techniczną.</span><span class="sxs-lookup"><span data-stu-id="6816f-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="6816f-114">Musisz określić następujące parametry:</span><span class="sxs-lookup"><span data-stu-id="6816f-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="6816f-115">Możesz użyć New-AzSupportContactProfileObject polecenia cmdlet pomocnika, aby utworzyć obiekt CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="6816f-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="6816f-116">Dostawcy rozwiązań w chmurze mogą utworzyć bilet pomocy technicznej dla abonamentów klienta, logując się do dzierżawy klienta i podając identyfikator dzierżawy domowej za pomocą parametru *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="6816f-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="6816f-117">__W przypadku biletów technicznych:__</span><span class="sxs-lookup"><span data-stu-id="6816f-117">__For technical tickets:__</span></span>

<span data-ttu-id="6816f-118">Aby określić nazwę zasobu, określ identyfikator zasobu ARM zasobu, używając parametru *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="6816f-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="6816f-119">Zobacz przykład poniżej.</span><span class="sxs-lookup"><span data-stu-id="6816f-119">See an example below.</span></span> 

<span data-ttu-id="6816f-120">__W przypadku biletów przydziałów:__</span><span class="sxs-lookup"><span data-stu-id="6816f-120">__For quota tickets:__</span></span>

<span data-ttu-id="6816f-121">Aby zażądać zwiększenia przydziału dla **rdzeni maszyny wirtualnej obliczeniowej**, **partii**, **bazy danych SQL** i usługi **SQL Data Warehouse**, podaj dodatkowe szczegóły w obszarze obiekt *QuotaTicketDetail* .</span><span class="sxs-lookup"><span data-stu-id="6816f-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="6816f-122">Obiekt QuotaTicketDetail składa się z trzech właściwości zgodnie z poniższym opisem.</span><span class="sxs-lookup"><span data-stu-id="6816f-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="6816f-123">Aby uzyskać szczegółową dokumentację, [kliknij tutaj.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="6816f-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="6816f-124">Aby uzyskać szczegółową dokumentację dotyczącą sposobu konstruowania ładunku dla różnych typów przydziałów, [kliknij tutaj](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="6816f-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="6816f-125">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6816f-125">EXAMPLES</span></span>

### <span data-ttu-id="6816f-126">Przykład 1: tworzenie biletu pomocy technicznej do zarządzania rozliczeniami lub abonamentami.</span><span class="sxs-lookup"><span data-stu-id="6816f-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="6816f-127">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemów z zarządzaniem rozliczeniami lub subskrypcjami, dla których chcesz uzyskać pomoc</span><span class="sxs-lookup"><span data-stu-id="6816f-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-128">Przykład 2: tworzenie biletu pomocy technicznej dla zasobu maszyna wirtualna dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="6816f-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="6816f-129">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla maszyny wirtualnej na potrzeby klasyfikacji problemów z systemem Windows, dla których chcesz uzyskać pomoc techniczną</span><span class="sxs-lookup"><span data-stu-id="6816f-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-130">Przykład 3: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału rdzeni maszyny wirtualnej dla konkretnej rodziny maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="6816f-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="6816f-131">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID na potrzeby obliczeń przydziału rdzenie maszyny wirtualnej z klasyfikacją.</span><span class="sxs-lookup"><span data-stu-id="6816f-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-132">Przykład 4: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału dla rozliczeń o niskim priorytecie dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6816f-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="6816f-133">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu partii zasobów.</span><span class="sxs-lookup"><span data-stu-id="6816f-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-134">Przykład 5: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału rdzeni maszyny wirtualnej dla określonej rodziny wirtualnych dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6816f-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="6816f-135">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu partii zasobów.</span><span class="sxs-lookup"><span data-stu-id="6816f-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-136">Przykład 6: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału pul dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6816f-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="6816f-137">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu partii zasobów.</span><span class="sxs-lookup"><span data-stu-id="6816f-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-138">Przykład 7: tworzenie biletu obsługi przydziałów w celu zwiększenia aktywnych zadań i harmonogramów zadań dla konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6816f-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="6816f-139">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu partii zasobów.</span><span class="sxs-lookup"><span data-stu-id="6816f-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-140">Przykład 8: tworzenie biletu obsługi przydziałów w celu zwiększenia liczby kont wsadowych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6816f-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="6816f-141">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu partii zasobów.</span><span class="sxs-lookup"><span data-stu-id="6816f-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-142">Przykład 9: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału dla bazy danych SQL DTU.</span><span class="sxs-lookup"><span data-stu-id="6816f-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="6816f-143">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla przydziałów o problemach z bazą danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-144">Przykład 10: tworzenie biletu obsługi przydziału w celu zwiększenia przydziału dla serwerów bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="6816f-145">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla przydziałów o problemach z bazą danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-146">Przykład 11: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału dla usługi DTU dla hurtowni danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="6816f-147">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu z usługą SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="6816f-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-148">Przykład 12: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału dla serwerów usługi SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="6816f-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="6816f-149">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu z magazynem danych SQL dotyczących przydziału.</span><span class="sxs-lookup"><span data-stu-id="6816f-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-150">Przykład 13: tworzenie biletu pomocy technicznej do przydziałów w celu zwiększenia przydziału w przypadku rdzeni o niskim priorytecie dla usługi szkolenia maszynowe.</span><span class="sxs-lookup"><span data-stu-id="6816f-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="6816f-151">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu z usługą Uczenie maszynowe.</span><span class="sxs-lookup"><span data-stu-id="6816f-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-152">Przykład 14: tworzenie biletu obsługi przydziałów w celu zwiększenia przydziału rdzeni maszyny wirtualnej dla konkretnej rodziny maszyn wirtualnych w usłudze Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="6816f-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="6816f-153">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla klasyfikacji problemu z usługą Uczenie maszynowe.</span><span class="sxs-lookup"><span data-stu-id="6816f-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-154">Przykład 15: tworzenie biletu pomocy technicznej przydziałów w celu zwiększenia przydziału wystąpienia zarządzanego w usłudze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="6816f-155">Użyj Get-AzSupportService i Get-AzSupportProblemClassification, aby pobrać właściwe identyfikatory GUID dla przydziału problemu z usługą zarządzanych wystąpień usługi SQL.</span><span class="sxs-lookup"><span data-stu-id="6816f-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-156">Przykład 16: tworzenie biletu pomocy technicznej przez określenie parametrów kontaktu poszczególnych klientów zamiast obiektu CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="6816f-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-157">Przykład 17: tworzenie biletu pomocy technicznej z prośbą o 24 x 7 odpowiedzi od platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6816f-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6816f-158">Przykład 18: tworzenie biletu pomocy technicznej w imieniu klienta, jeśli jesteś dostawcą rozwiązań w chmurze (CSP).</span><span class="sxs-lookup"><span data-stu-id="6816f-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="6816f-159">Dostawca CSP powinien najpierw zalogować się do dzierżawy, a następnie zalogować się do dzierżawy klienta, jak pokazano w poniższym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="6816f-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="6816f-160">Aby określić identyfikator dzierżawy domowej w momencie tworzenia biletu pomocy technicznej, należy użyć parametru-CSPHomeTenantId.</span><span class="sxs-lookup"><span data-stu-id="6816f-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="6816f-161">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6816f-161">PARAMETERS</span></span>

### <span data-ttu-id="6816f-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6816f-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="6816f-163">Dodatkowe adresy e-mail.</span><span class="sxs-lookup"><span data-stu-id="6816f-163">Additional email addresses.</span></span>
<span data-ttu-id="6816f-164">Adresy e-mail wymienione tutaj zostaną skopiowane w dowolnej korespondencji na temat biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="6816f-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="6816f-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6816f-165">-AsJob</span></span>
<span data-ttu-id="6816f-166">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="6816f-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6816f-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="6816f-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="6816f-168">Jest to identyfikator dzierżawy domowej użytkownika dostawcy rozwiązań w chmurze próbującej utworzyć bilet pomocy technicznej dla klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="6816f-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="6816f-169">-CustomerContactDetail</span></span>
<span data-ttu-id="6816f-170">Szczegółowe dane kontaktowe klienta skojarzone z zasobem SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="6816f-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="6816f-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="6816f-171">-CustomerCountry</span></span>
<span data-ttu-id="6816f-172">Kraj klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-172">Customer country.</span></span>
<span data-ttu-id="6816f-173">Musi to być prawidłowy kod kraju ISO alfa-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="6816f-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="6816f-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="6816f-174">-CustomerFirstName</span></span>
<span data-ttu-id="6816f-175">Imię i nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-175">Customer first name.</span></span>

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

### <span data-ttu-id="6816f-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="6816f-176">-CustomerLastName</span></span>
<span data-ttu-id="6816f-177">Nazwisko klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-177">Customer last name.</span></span>

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

### <span data-ttu-id="6816f-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6816f-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="6816f-179">Numer telefonu klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-179">Customer phone number.</span></span>
<span data-ttu-id="6816f-180">Jest to wymagane, jeśli preferowaną metodą kontaktu jest telefon.</span><span class="sxs-lookup"><span data-stu-id="6816f-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="6816f-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="6816f-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="6816f-182">Peferred język niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="6816f-182">Peferred language of the custom.</span></span>
<span data-ttu-id="6816f-183">Musi to być prawidłowy kod językowy dla jednego z obsługiwanych języków z listy https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="6816f-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="6816f-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="6816f-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="6816f-185">Preferowana strefa czasowa klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-185">Customer preferred time zone.</span></span>
<span data-ttu-id="6816f-186">Ta wartość musi być prawidłową wartością System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="6816f-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="6816f-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6816f-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="6816f-188">Podstawowy adres e-mail klienta.</span><span class="sxs-lookup"><span data-stu-id="6816f-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="6816f-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6816f-189">-DefaultProfile</span></span>
<span data-ttu-id="6816f-190">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6816f-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6816f-191">— Opis</span><span class="sxs-lookup"><span data-stu-id="6816f-191">-Description</span></span>
<span data-ttu-id="6816f-192">Szczegółowy opis pytania lub problemu.</span><span class="sxs-lookup"><span data-stu-id="6816f-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="6816f-193">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6816f-193">-Name</span></span>
<span data-ttu-id="6816f-194">Nazwa biletu pomocy technicznej tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6816f-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6816f-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="6816f-195">-PreferredContactMethod</span></span>
<span data-ttu-id="6816f-196">Preferowana metoda kontaktu.</span><span class="sxs-lookup"><span data-stu-id="6816f-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="6816f-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="6816f-197">-ProblemClassificationId</span></span>
<span data-ttu-id="6816f-198">Każda usługa Azure ma swoją własną kategorię problemu o nazwie Klasyfikacja problemu, która odpowiada typowi napotkanych problemów.</span><span class="sxs-lookup"><span data-stu-id="6816f-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="6816f-199">Ten parametr jest identyfikatorem zasobu ARM ProblemClassification Resource.</span><span class="sxs-lookup"><span data-stu-id="6816f-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="6816f-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="6816f-200">-ProblemStartTime</span></span>
<span data-ttu-id="6816f-201">Data i godzina rozpoczęcia problemu.</span><span class="sxs-lookup"><span data-stu-id="6816f-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="6816f-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="6816f-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="6816f-203">Dodatkowe informacje dotyczące biletu obsługi przydziału.</span><span class="sxs-lookup"><span data-stu-id="6816f-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="6816f-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="6816f-204">-Require24X7Response</span></span>
<span data-ttu-id="6816f-205">Wskazuje, czy ten bilet pomocy technicznej wymaga odpowiedzi na 24x7 z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6816f-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="6816f-206">— Ważność</span><span class="sxs-lookup"><span data-stu-id="6816f-206">-Severity</span></span>
<span data-ttu-id="6816f-207">Ważność biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="6816f-207">Severity of the support ticket.</span></span>
<span data-ttu-id="6816f-208">Wskazuje to na pilność sprawy, która z kolei decyduje o czasie reakcji zgodnie z umową dotyczącą poziomu usług w planie pomocy technicznej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6816f-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="6816f-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="6816f-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="6816f-210">Jest to identyfikator zasobu usługi platformy Azure (na przykład: zasób maszyny wirtualnej lub zasób usługi HDInsight), dla którego został utworzony bilet pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="6816f-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="6816f-211">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="6816f-211">-Title</span></span>
<span data-ttu-id="6816f-212">Tytuł biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="6816f-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="6816f-213">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6816f-213">-Confirm</span></span>
<span data-ttu-id="6816f-214">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6816f-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6816f-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6816f-215">-WhatIf</span></span>
<span data-ttu-id="6816f-216">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6816f-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6816f-217">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6816f-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6816f-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6816f-218">CommonParameters</span></span>
<span data-ttu-id="6816f-219">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6816f-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6816f-220">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6816f-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6816f-221">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6816f-221">INPUTS</span></span>

### <span data-ttu-id="6816f-222">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6816f-222">None</span></span>

## <span data-ttu-id="6816f-223">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6816f-223">OUTPUTS</span></span>

### <span data-ttu-id="6816f-224">Microsoft. Azure. Commands. support. models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6816f-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6816f-225">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6816f-225">NOTES</span></span>

## <span data-ttu-id="6816f-226">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6816f-226">RELATED LINKS</span></span>

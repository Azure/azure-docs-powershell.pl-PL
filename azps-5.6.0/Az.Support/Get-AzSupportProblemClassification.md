---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: 0c8bf7d7a8217ed63920495591f8ad061f1b0a8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972497"
---
# <span data-ttu-id="35086-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="35086-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="35086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35086-102">SYNOPSIS</span></span>
<span data-ttu-id="35086-103">Uzyskaj klasyfikacje problemów dla określonej usługi.</span><span class="sxs-lookup"><span data-stu-id="35086-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="35086-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35086-104">SYNTAX</span></span>

### <span data-ttu-id="35086-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="35086-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35086-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35086-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35086-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="35086-107">DESCRIPTION</span></span>
<span data-ttu-id="35086-108">Pobiera bieżącą listę klasyfikacji problemów dla usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="35086-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="35086-109">Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-azSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="35086-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="35086-110">Identyfikatory GUID klasyfikacji usługi i problemu zawsze należy stosować programowo.</span><span class="sxs-lookup"><span data-stu-id="35086-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="35086-111">Takie rozwiązanie zapewnia, że masz najnowszy zestaw usług i identyfikatory GUID klasyfikacji problemów do tworzenia biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="35086-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="35086-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35086-112">EXAMPLES</span></span>

### <span data-ttu-id="35086-113">Przykład 1. Uzyskiwanie wszystkich opisów problemów dla usługi przy użyciu parametru identyfikatora usługi.</span><span class="sxs-lookup"><span data-stu-id="35086-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="35086-114">Przykład 2. Uzyskiwanie wszystkich opisów problemów dla usługi używającej nadrzędnego obiektu usługi</span><span class="sxs-lookup"><span data-stu-id="35086-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="35086-115">Przykład 3. Uzyskiwanie szczegółowych informacji o pojedynczym problemie classificaiton by id przez obiekt usługi piping</span><span class="sxs-lookup"><span data-stu-id="35086-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="35086-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35086-116">PARAMETERS</span></span>

### <span data-ttu-id="35086-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35086-117">-DefaultProfile</span></span>
<span data-ttu-id="35086-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35086-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35086-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="35086-119">-Id</span></span>
<span data-ttu-id="35086-120">Identyfikator klasyfikacji problemu.</span><span class="sxs-lookup"><span data-stu-id="35086-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35086-121">- ServiceId</span><span class="sxs-lookup"><span data-stu-id="35086-121">-ServiceId</span></span>
<span data-ttu-id="35086-122">Identyfikator usługi, dla którego są pobierane wszystkie klasyfikacje problemów.</span><span class="sxs-lookup"><span data-stu-id="35086-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35086-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="35086-123">-ServiceObject</span></span>
<span data-ttu-id="35086-124">Obiekt usługi, dla którego są pobierane klasyfikacje problemów.</span><span class="sxs-lookup"><span data-stu-id="35086-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35086-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35086-125">CommonParameters</span></span>
<span data-ttu-id="35086-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35086-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35086-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35086-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35086-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35086-128">INPUTS</span></span>

### <span data-ttu-id="35086-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="35086-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="35086-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35086-130">OUTPUTS</span></span>

### <span data-ttu-id="35086-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="35086-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="35086-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35086-132">NOTES</span></span>

## <span data-ttu-id="35086-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35086-133">RELATED LINKS</span></span>

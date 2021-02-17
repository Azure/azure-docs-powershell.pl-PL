---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190659"
---
# <span data-ttu-id="c8d15-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="c8d15-101">Get-AzSupportService</span></span>

## <span data-ttu-id="c8d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d15-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d15-103">Uzyskaj usługi, dla których jest dostępna pomoc techniczna.</span><span class="sxs-lookup"><span data-stu-id="c8d15-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="c8d15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8d15-104">SYNTAX</span></span>

### <span data-ttu-id="c8d15-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c8d15-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8d15-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d15-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d15-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8d15-107">DESCRIPTION</span></span>
<span data-ttu-id="c8d15-108">Pobiera bieżącą listę usług platformy Azure, dla których jest dostępna pomoc techniczna.</span><span class="sxs-lookup"><span data-stu-id="c8d15-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="c8d15-109">Każda usługa może zawierać co najmniej jedną informację o typie zasobów menedżera zasobów platformy Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="c8d15-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="c8d15-110">Typy zasobów (na przykład " microsoft.compute/virtualmachines") mogą być przydatne do zamapowania odpowiedniego produktu i zasobu ARM podczas tworzenia biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="c8d15-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="c8d15-111">Każda usługa Azure ma własny zestaw kategorii nazywany klasyfikacją problemu.</span><span class="sxs-lookup"><span data-stu-id="c8d15-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="c8d15-112">Pobierz bieżącą listę klasyfikacji problemów dla usługi za pomocą funkcji Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="c8d15-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="c8d15-113">Za pomocą identyfikatora GUID klasyfikacji usługi i problemu możesz utworzyć nowy bilet pomocy technicznej przy użyciu new-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="c8d15-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="c8d15-114">Identyfikatory GUID klasyfikacji usługi i problemu zawsze należy stosować programowo.</span><span class="sxs-lookup"><span data-stu-id="c8d15-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="c8d15-115">Takie rozwiązanie zapewnia, że masz najnowszy zestaw usług i identyfikatory GUID klasyfikacji problemów do tworzenia biletu pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="c8d15-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="c8d15-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8d15-116">EXAMPLES</span></span>

### <span data-ttu-id="c8d15-117">Przykład 1. Uzyskiwanie pomocy technicznej dla wszystkich usług</span><span class="sxs-lookup"><span data-stu-id="c8d15-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="c8d15-118">Przykład 2. Uzyskiwanie szczegółowych informacji o pojedynczej usłudze według identyfikatora dostępnego w celu uzyskania pomocy technicznej</span><span class="sxs-lookup"><span data-stu-id="c8d15-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="c8d15-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8d15-119">PARAMETERS</span></span>

### <span data-ttu-id="c8d15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d15-120">-DefaultProfile</span></span>
<span data-ttu-id="c8d15-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d15-122">— Id</span><span class="sxs-lookup"><span data-stu-id="c8d15-122">-Id</span></span>
<span data-ttu-id="c8d15-123">Identyfikator usługi.</span><span class="sxs-lookup"><span data-stu-id="c8d15-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d15-124">CommonParameters</span></span>
<span data-ttu-id="c8d15-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d15-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8d15-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d15-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8d15-127">INPUTS</span></span>

### <span data-ttu-id="c8d15-128">Brak</span><span class="sxs-lookup"><span data-stu-id="c8d15-128">None</span></span>

## <span data-ttu-id="c8d15-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8d15-129">OUTPUTS</span></span>

### <span data-ttu-id="c8d15-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="c8d15-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="c8d15-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8d15-131">NOTES</span></span>

## <span data-ttu-id="c8d15-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8d15-132">RELATED LINKS</span></span>

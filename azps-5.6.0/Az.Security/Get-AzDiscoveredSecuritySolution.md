---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d351ab76941d16e3d3e091e223524863d4256d75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986588"
---
# <span data-ttu-id="81ba4-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="81ba4-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="81ba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="81ba4-103">Pobiera rozwiązania zabezpieczeń odkryte przez Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="81ba4-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="81ba4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81ba4-104">SYNTAX</span></span>

### <span data-ttu-id="81ba4-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="81ba4-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81ba4-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="81ba4-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81ba4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81ba4-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81ba4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="81ba4-108">DESCRIPTION</span></span>
<span data-ttu-id="81ba4-109">Rozwiązania zabezpieczeń są automatycznie wykrywane przez Usługę Azure Security Center. To polecenie cmdlet umożliwia wyświetlenie wykrytych rozwiązań zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="81ba4-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="81ba4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="81ba4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81ba4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="81ba4-112">Uzyskiwanie wszystkich wykrytych rozwiązań zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="81ba4-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="81ba4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="81ba4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="81ba4-114">Uzyskiwanie konkretnego wykrytego rozwiązania zabezpieczającego</span><span class="sxs-lookup"><span data-stu-id="81ba4-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="81ba4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81ba4-115">PARAMETERS</span></span>

### <span data-ttu-id="81ba4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ba4-116">-DefaultProfile</span></span>
<span data-ttu-id="81ba4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81ba4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81ba4-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="81ba4-118">-Location</span></span>
<span data-ttu-id="81ba4-119">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="81ba4-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ba4-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81ba4-120">-Name</span></span>
<span data-ttu-id="81ba4-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="81ba4-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ba4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ba4-122">-ResourceGroupName</span></span>
<span data-ttu-id="81ba4-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81ba4-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ba4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81ba4-124">-ResourceId</span></span>
<span data-ttu-id="81ba4-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="81ba4-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ba4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ba4-126">CommonParameters</span></span>
<span data-ttu-id="81ba4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ba4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ba4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81ba4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ba4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81ba4-129">INPUTS</span></span>

### <span data-ttu-id="81ba4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="81ba4-130">System.String</span></span>

## <span data-ttu-id="81ba4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81ba4-131">OUTPUTS</span></span>

### <span data-ttu-id="81ba4-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="81ba4-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="81ba4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81ba4-133">NOTES</span></span>

## <span data-ttu-id="81ba4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81ba4-134">RELATED LINKS</span></span>

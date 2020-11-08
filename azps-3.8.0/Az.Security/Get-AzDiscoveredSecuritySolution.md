---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: e81224796d8f38f15d8c3a08e5b572c8f3aab117
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053652"
---
# <span data-ttu-id="3e665-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3e665-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3e665-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e665-102">SYNOPSIS</span></span>
<span data-ttu-id="3e665-103">Pobieranie rozwiązań zabezpieczeń, które zostały wykryte przez usługę Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="3e665-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="3e665-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e665-104">SYNTAX</span></span>

### <span data-ttu-id="3e665-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e665-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e665-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e665-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e665-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3e665-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e665-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e665-108">DESCRIPTION</span></span>
<span data-ttu-id="3e665-109">Rozwiązania dotyczące zabezpieczeń są automatycznie wykrywane przez usługę Azure Security Center, to polecenie cmdlet służy do wyświetlania odnalezionych rozwiązań zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="3e665-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="3e665-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e665-110">EXAMPLES</span></span>

### <span data-ttu-id="3e665-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e665-111">Example 1</span></span>
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

<span data-ttu-id="3e665-112">Uzyskaj wszystkie wykryte rozwiązania dotyczące zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e665-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="3e665-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e665-113">Example 2</span></span>
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

<span data-ttu-id="3e665-114">Uzyskiwanie określonego wykrytego rozwiązania dotyczącego zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="3e665-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="3e665-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e665-115">PARAMETERS</span></span>

### <span data-ttu-id="3e665-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e665-116">-DefaultProfile</span></span>
<span data-ttu-id="3e665-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e665-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e665-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e665-118">-Location</span></span>
<span data-ttu-id="3e665-119">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="3e665-119">Location.</span></span>

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

### <span data-ttu-id="3e665-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e665-120">-Name</span></span>
<span data-ttu-id="3e665-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e665-121">Resource name.</span></span>

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

### <span data-ttu-id="3e665-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e665-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e665-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e665-123">Resource group name.</span></span>

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

### <span data-ttu-id="3e665-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e665-124">-ResourceId</span></span>
<span data-ttu-id="3e665-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e665-125">Resource ID.</span></span>

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

### <span data-ttu-id="3e665-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e665-126">CommonParameters</span></span>
<span data-ttu-id="3e665-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e665-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e665-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e665-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e665-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e665-129">INPUTS</span></span>

### <span data-ttu-id="3e665-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e665-130">System.String</span></span>

## <span data-ttu-id="3e665-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e665-131">OUTPUTS</span></span>

### <span data-ttu-id="3e665-132">Microsoft. Azure. Commands. Security. models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3e665-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3e665-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e665-133">NOTES</span></span>

## <span data-ttu-id="3e665-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e665-134">RELATED LINKS</span></span>

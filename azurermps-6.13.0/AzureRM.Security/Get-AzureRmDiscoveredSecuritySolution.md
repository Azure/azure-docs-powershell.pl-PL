---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543455"
---
# <span data-ttu-id="5c8d0-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5c8d0-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5c8d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8d0-103">Pobieranie rozwiązań zabezpieczeń, które zostały wykryte przez usługę Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="5c8d0-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c8d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c8d0-104">SYNTAX</span></span>

### <span data-ttu-id="5c8d0-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c8d0-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8d0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5c8d0-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8d0-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5c8d0-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c8d0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5c8d0-108">DESCRIPTION</span></span>
<span data-ttu-id="5c8d0-109">Rozwiązania dotyczące zabezpieczeń są automatycznie wykrywane przez usługę Azure Security Center, to polecenie cmdlet służy do wyświetlania odnalezionych rozwiązań zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5c8d0-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="5c8d0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c8d0-110">EXAMPLES</span></span>

### <span data-ttu-id="5c8d0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c8d0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5c8d0-112">Uzyskaj wszystkie wykryte rozwiązania dotyczące zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5c8d0-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="5c8d0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c8d0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5c8d0-114">Uzyskiwanie określonego wykrytego rozwiązania dotyczącego zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5c8d0-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="5c8d0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c8d0-115">PARAMETERS</span></span>

### <span data-ttu-id="5c8d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8d0-116">-DefaultProfile</span></span>
<span data-ttu-id="5c8d0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8d0-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5c8d0-118">-Location</span></span>
<span data-ttu-id="5c8d0-119">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8d0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c8d0-120">-Name</span></span>
<span data-ttu-id="5c8d0-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c8d0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8d0-124">-ResourceId</span></span>
<span data-ttu-id="5c8d0-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-125">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c8d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8d0-126">CommonParameters</span></span>
<span data-ttu-id="5c8d0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8d0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c8d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8d0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c8d0-129">INPUTS</span></span>

### <span data-ttu-id="5c8d0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c8d0-130">System.String</span></span>

## <span data-ttu-id="5c8d0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c8d0-131">OUTPUTS</span></span>

### <span data-ttu-id="5c8d0-132">Microsoft. Azure. Commands. Security. models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5c8d0-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5c8d0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c8d0-133">NOTES</span></span>

## <span data-ttu-id="5c8d0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c8d0-134">RELATED LINKS</span></span>

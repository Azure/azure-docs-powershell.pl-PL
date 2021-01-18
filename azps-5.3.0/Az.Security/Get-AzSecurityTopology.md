---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503031"
---
# <span data-ttu-id="a84f1-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="a84f1-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="a84f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a84f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a84f1-103">Pobiera listę topologii zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a84f1-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="a84f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a84f1-104">SYNTAX</span></span>

### <span data-ttu-id="a84f1-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a84f1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84f1-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a84f1-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84f1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a84f1-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a84f1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a84f1-108">DESCRIPTION</span></span>
<span data-ttu-id="a84f1-109">Topologie zabezpieczeń są automatycznie wykrywane przez usługę Azure Security Center, użyj tego polecenia cmdlet, aby wyświetlić topologie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="a84f1-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="a84f1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a84f1-110">EXAMPLES</span></span>

### <span data-ttu-id="a84f1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a84f1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="a84f1-112">Wyświetlanie wszystkich topologii zabezpieczeń w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a84f1-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="a84f1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a84f1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="a84f1-114">Uzyskiwanie określonych topologii zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="a84f1-114">Get a specific security topologies</span></span>

## <span data-ttu-id="a84f1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a84f1-115">PARAMETERS</span></span>

### <span data-ttu-id="a84f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84f1-116">-DefaultProfile</span></span>
<span data-ttu-id="a84f1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a84f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a84f1-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a84f1-118">-Location</span></span>
<span data-ttu-id="a84f1-119">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="a84f1-119">Location.</span></span>

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

### <span data-ttu-id="a84f1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a84f1-120">-Name</span></span>
<span data-ttu-id="a84f1-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a84f1-121">Resource name.</span></span>

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

### <span data-ttu-id="a84f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="a84f1-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a84f1-123">Resource group name.</span></span>

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

### <span data-ttu-id="a84f1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a84f1-124">-ResourceId</span></span>
<span data-ttu-id="a84f1-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a84f1-125">Resource ID.</span></span>

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

### <span data-ttu-id="a84f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84f1-126">CommonParameters</span></span>
<span data-ttu-id="a84f1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84f1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84f1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84f1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a84f1-129">INPUTS</span></span>

### <span data-ttu-id="a84f1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a84f1-130">System.String</span></span>

## <span data-ttu-id="a84f1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a84f1-131">OUTPUTS</span></span>

### <span data-ttu-id="a84f1-132">Microsoft. Azure. Commands. Security. MODELES. Topology. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="a84f1-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="a84f1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a84f1-133">NOTES</span></span>

## <span data-ttu-id="a84f1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a84f1-134">RELATED LINKS</span></span>

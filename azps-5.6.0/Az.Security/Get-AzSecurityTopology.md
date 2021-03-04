---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990753"
---
# <span data-ttu-id="e104f-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="e104f-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="e104f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e104f-102">SYNOPSIS</span></span>
<span data-ttu-id="e104f-103">Pobiera listę topologii zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e104f-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="e104f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e104f-104">SYNTAX</span></span>

### <span data-ttu-id="e104f-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e104f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e104f-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e104f-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e104f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e104f-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e104f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e104f-108">DESCRIPTION</span></span>
<span data-ttu-id="e104f-109">Usługa Azure Security Center automatycznie wykrywa topologii zabezpieczeń. To polecenie cmdlet umożliwia wyświetlanie topologii zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="e104f-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="e104f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e104f-110">EXAMPLES</span></span>

### <span data-ttu-id="e104f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e104f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e104f-112">Wyświetlanie wszystkich topologii zabezpieczeń w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e104f-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="e104f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e104f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e104f-114">Uzyskiwanie określonych topologii zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="e104f-114">Get a specific security topologies</span></span>

## <span data-ttu-id="e104f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e104f-115">PARAMETERS</span></span>

### <span data-ttu-id="e104f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e104f-116">-DefaultProfile</span></span>
<span data-ttu-id="e104f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e104f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e104f-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e104f-118">-Location</span></span>
<span data-ttu-id="e104f-119">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="e104f-119">Location.</span></span>

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

### <span data-ttu-id="e104f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e104f-120">-Name</span></span>
<span data-ttu-id="e104f-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e104f-121">Resource name.</span></span>

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

### <span data-ttu-id="e104f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e104f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e104f-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e104f-123">Resource group name.</span></span>

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

### <span data-ttu-id="e104f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e104f-124">-ResourceId</span></span>
<span data-ttu-id="e104f-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e104f-125">Resource ID.</span></span>

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

### <span data-ttu-id="e104f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e104f-126">CommonParameters</span></span>
<span data-ttu-id="e104f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e104f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e104f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e104f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e104f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e104f-129">INPUTS</span></span>

### <span data-ttu-id="e104f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e104f-130">System.String</span></span>

## <span data-ttu-id="e104f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e104f-131">OUTPUTS</span></span>

### <span data-ttu-id="e104f-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="e104f-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="e104f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e104f-133">NOTES</span></span>

## <span data-ttu-id="e104f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e104f-134">RELATED LINKS</span></span>

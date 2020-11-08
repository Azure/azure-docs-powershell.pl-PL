---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222994"
---
# <span data-ttu-id="2e0d2-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2e0d2-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="2e0d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0d2-103">Pobiera listę prefiksów usługi peer dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="2e0d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e0d2-104">SYNTAX</span></span>

### <span data-ttu-id="2e0d2-105">ByResourceGroupAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e0d2-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e0d2-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e0d2-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e0d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e0d2-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e0d2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e0d2-108">DESCRIPTION</span></span>
<span data-ttu-id="2e0d2-109">Wyświetlanie prefiksów usługi peer resystems dla obiektów usługi peer</span><span class="sxs-lookup"><span data-stu-id="2e0d2-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="2e0d2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="2e0d2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e0d2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="2e0d2-112">Pobiera prefiksy dla usługi peer na podstawie poleceń połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="2e0d2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e0d2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="2e0d2-114">Pobiera określony prefiks usługi peer na identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="2e0d2-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2e0d2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="2e0d2-116">Pobiera określony prefiks usługi peer na identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="2e0d2-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="2e0d2-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="2e0d2-118">Pobiera określony prefiks usługi peer with rozszerzone atrybuty</span><span class="sxs-lookup"><span data-stu-id="2e0d2-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="2e0d2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e0d2-119">PARAMETERS</span></span>

### <span data-ttu-id="2e0d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0d2-120">-DefaultProfile</span></span>
<span data-ttu-id="2e0d2-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e0d2-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="2e0d2-122">-Expand</span></span>
<span data-ttu-id="2e0d2-123">Wyświetlanie zdarzeń dotyczących prefiksu usługi peer</span><span class="sxs-lookup"><span data-stu-id="2e0d2-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="2e0d2-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e0d2-124">-Name</span></span>
<span data-ttu-id="2e0d2-125">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e0d2-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="2e0d2-126">-PeeringServiceName</span></span>
<span data-ttu-id="2e0d2-127">Nazwa usługi peer.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-127">The peering service name.</span></span> <span data-ttu-id="2e0d2-128">Użyj polecenia cmdlet New-AzPeeringService dla nowej usługi peer lub Get-AzPeeringService listy.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e0d2-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="2e0d2-129">-PeeringServiceObject</span></span>
<span data-ttu-id="2e0d2-130">Używanie Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="2e0d2-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="2e0d2-132">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e0d2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e0d2-133">-ResourceId</span></span>
<span data-ttu-id="2e0d2-134">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e0d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0d2-135">CommonParameters</span></span>
<span data-ttu-id="2e0d2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0d2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e0d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0d2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e0d2-138">INPUTS</span></span>

### <span data-ttu-id="2e0d2-139">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="2e0d2-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="2e0d2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0d2-140">System.String</span></span>

## <span data-ttu-id="2e0d2-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e0d2-141">OUTPUTS</span></span>

### <span data-ttu-id="2e0d2-142">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="2e0d2-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="2e0d2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e0d2-143">NOTES</span></span>

## <span data-ttu-id="2e0d2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e0d2-144">RELATED LINKS</span></span>

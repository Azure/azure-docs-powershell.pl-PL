---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238919"
---
# <span data-ttu-id="b535f-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="b535f-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="b535f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b535f-102">SYNOPSIS</span></span>
<span data-ttu-id="b535f-103">Pobierz hosty lub wybierz ich listę.</span><span class="sxs-lookup"><span data-stu-id="b535f-103">Get or list hosts.</span></span>

## <span data-ttu-id="b535f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b535f-104">SYNTAX</span></span>

### <span data-ttu-id="b535f-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b535f-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b535f-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="b535f-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b535f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b535f-107">DESCRIPTION</span></span>
<span data-ttu-id="b535f-108">To polecenie cmdlet pobierze grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="b535f-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="b535f-109">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w grupie zasobów, jeśli nazwa grupy hosta nie zostanie nadana.</span><span class="sxs-lookup"><span data-stu-id="b535f-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="b535f-110">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w subskrypcji, jeśli nie podano nazwy grupy ani nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b535f-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="b535f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b535f-111">EXAMPLES</span></span>

### <span data-ttu-id="b535f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b535f-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="b535f-113">To polecenie zwraca grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="b535f-113">This command returns a host group.</span></span>

### <span data-ttu-id="b535f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b535f-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="b535f-115">To polecenie zwraca wszystkie grupy hostów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b535f-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="b535f-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b535f-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="b535f-117">To polecenie zwraca wszystkie grupy hostów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b535f-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="b535f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b535f-118">PARAMETERS</span></span>

### <span data-ttu-id="b535f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b535f-119">-DefaultProfile</span></span>
<span data-ttu-id="b535f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b535f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b535f-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b535f-121">-InstanceView</span></span>
<span data-ttu-id="b535f-122">Rozwiń zwrócony obiekt, aby wyświetlić również widoki wystąpienia hosta.</span><span class="sxs-lookup"><span data-stu-id="b535f-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b535f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b535f-123">-Name</span></span>
<span data-ttu-id="b535f-124">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="b535f-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b535f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b535f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b535f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b535f-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b535f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b535f-127">-ResourceId</span></span>
<span data-ttu-id="b535f-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b535f-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b535f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b535f-129">CommonParameters</span></span>
<span data-ttu-id="b535f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b535f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b535f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b535f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b535f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b535f-132">INPUTS</span></span>

### <span data-ttu-id="b535f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b535f-133">System.String</span></span>

## <span data-ttu-id="b535f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b535f-134">OUTPUTS</span></span>

### <span data-ttu-id="b535f-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="b535f-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="b535f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b535f-136">NOTES</span></span>

## <span data-ttu-id="b535f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b535f-137">RELATED LINKS</span></span>

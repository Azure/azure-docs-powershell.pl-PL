---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991523"
---
# <span data-ttu-id="92bb9-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="92bb9-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="92bb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="92bb9-103">Pobierz hosty lub przygotuj ich listę.</span><span class="sxs-lookup"><span data-stu-id="92bb9-103">Get or list hosts.</span></span>

## <span data-ttu-id="92bb9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92bb9-104">SYNTAX</span></span>

### <span data-ttu-id="92bb9-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92bb9-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92bb9-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="92bb9-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92bb9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="92bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="92bb9-108">To polecenie cmdlet pobierze grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="92bb9-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="92bb9-109">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w grupie zasobów, jeśli nazwa grupy hosta nie zostanie nadana.</span><span class="sxs-lookup"><span data-stu-id="92bb9-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="92bb9-110">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w subskrypcji, jeśli nie podano nazwy ani nazwy grupy hostów, ani nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92bb9-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="92bb9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92bb9-111">EXAMPLES</span></span>

### <span data-ttu-id="92bb9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92bb9-112">Example 1</span></span>
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

<span data-ttu-id="92bb9-113">To polecenie zwraca grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="92bb9-113">This command returns a host group.</span></span>

### <span data-ttu-id="92bb9-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="92bb9-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="92bb9-115">To polecenie zwraca wszystkie grupy hostów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="92bb9-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="92bb9-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="92bb9-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="92bb9-117">To polecenie zwraca wszystkie grupy hostów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="92bb9-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="92bb9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92bb9-118">PARAMETERS</span></span>

### <span data-ttu-id="92bb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bb9-119">-DefaultProfile</span></span>
<span data-ttu-id="92bb9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92bb9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92bb9-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="92bb9-121">-InstanceView</span></span>
<span data-ttu-id="92bb9-122">Rozwiń zwrócony obiekt, aby również wyświetlić listę widoków wystąpienia hosta.</span><span class="sxs-lookup"><span data-stu-id="92bb9-122">Expand the returned object to also list the host's instance views.</span></span> 

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

### <span data-ttu-id="92bb9-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92bb9-123">-Name</span></span>
<span data-ttu-id="92bb9-124">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="92bb9-124">The name of the host group.</span></span>

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

### <span data-ttu-id="92bb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="92bb9-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92bb9-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="92bb9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92bb9-127">-ResourceId</span></span>
<span data-ttu-id="92bb9-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="92bb9-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="92bb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bb9-129">CommonParameters</span></span>
<span data-ttu-id="92bb9-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bb9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92bb9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bb9-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92bb9-132">INPUTS</span></span>

### <span data-ttu-id="92bb9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="92bb9-133">System.String</span></span>

## <span data-ttu-id="92bb9-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92bb9-134">OUTPUTS</span></span>

### <span data-ttu-id="92bb9-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="92bb9-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="92bb9-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92bb9-136">NOTES</span></span>

## <span data-ttu-id="92bb9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92bb9-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332338"
---
# <span data-ttu-id="92887-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="92887-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="92887-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92887-102">SYNOPSIS</span></span>
<span data-ttu-id="92887-103">Pobierz lub wystaw Hosts.</span><span class="sxs-lookup"><span data-stu-id="92887-103">Get or list hosts.</span></span>

## <span data-ttu-id="92887-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92887-104">SYNTAX</span></span>

### <span data-ttu-id="92887-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92887-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92887-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="92887-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92887-107">Opis</span><span class="sxs-lookup"><span data-stu-id="92887-107">DESCRIPTION</span></span>
<span data-ttu-id="92887-108">To polecenie cmdlet spowoduje wyświetlenie grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="92887-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="92887-109">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w grupie zasobów, jeśli nie podano nazwy grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="92887-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="92887-110">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w subskrypcji, jeśli nie podano nazwy grupy hostów ani nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92887-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="92887-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92887-111">EXAMPLES</span></span>

### <span data-ttu-id="92887-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92887-112">Example 1</span></span>
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

<span data-ttu-id="92887-113">To polecenie zwraca grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="92887-113">This command returns a host group.</span></span>

### <span data-ttu-id="92887-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="92887-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="92887-115">To polecenie zwraca wszystkie grupy hostów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="92887-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="92887-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="92887-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="92887-117">To polecenie zwraca wszystkie grupy hostów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="92887-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="92887-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92887-118">PARAMETERS</span></span>

### <span data-ttu-id="92887-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92887-119">-DefaultProfile</span></span>
<span data-ttu-id="92887-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92887-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92887-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="92887-121">-InstanceView</span></span>
<span data-ttu-id="92887-122">Rozwiń zwrócony obiekt, aby wyświetlić również widoki wystąpienia hosta.</span><span class="sxs-lookup"><span data-stu-id="92887-122">Expand the returned object to also list the host's instance views.</span></span> 

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

### <span data-ttu-id="92887-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92887-123">-Name</span></span>
<span data-ttu-id="92887-124">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="92887-124">The name of the host group.</span></span>

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

### <span data-ttu-id="92887-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92887-125">-ResourceGroupName</span></span>
<span data-ttu-id="92887-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92887-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="92887-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92887-127">-ResourceId</span></span>
<span data-ttu-id="92887-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="92887-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="92887-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92887-129">CommonParameters</span></span>
<span data-ttu-id="92887-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92887-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92887-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92887-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92887-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92887-132">INPUTS</span></span>

### <span data-ttu-id="92887-133">System. String</span><span class="sxs-lookup"><span data-stu-id="92887-133">System.String</span></span>

## <span data-ttu-id="92887-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92887-134">OUTPUTS</span></span>

### <span data-ttu-id="92887-135">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="92887-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="92887-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92887-136">NOTES</span></span>

## <span data-ttu-id="92887-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92887-137">RELATED LINKS</span></span>

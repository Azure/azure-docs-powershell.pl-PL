---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706438"
---
# <span data-ttu-id="ea29a-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="ea29a-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="ea29a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea29a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea29a-103">Pobierz lub wystaw Hosts.</span><span class="sxs-lookup"><span data-stu-id="ea29a-103">Get or list hosts.</span></span>

## <span data-ttu-id="ea29a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea29a-104">SYNTAX</span></span>

### <span data-ttu-id="ea29a-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea29a-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea29a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ea29a-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea29a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea29a-107">DESCRIPTION</span></span>
<span data-ttu-id="ea29a-108">To polecenie cmdlet spowoduje wyświetlenie grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="ea29a-109">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w grupie zasobów, jeśli nie podano nazwy grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="ea29a-110">To polecenie cmdlet wyświetla również listę wszystkich grup hostów w subskrypcji, jeśli nie podano nazwy grupy hostów ani nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="ea29a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea29a-111">EXAMPLES</span></span>

### <span data-ttu-id="ea29a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea29a-112">Example 1</span></span>
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

<span data-ttu-id="ea29a-113">To polecenie zwraca grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-113">This command returns a host group.</span></span>

### <span data-ttu-id="ea29a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ea29a-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="ea29a-115">To polecenie zwraca wszystkie grupy hostów w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="ea29a-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ea29a-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="ea29a-117">To polecenie zwraca wszystkie grupy hostów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ea29a-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="ea29a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea29a-118">PARAMETERS</span></span>

### <span data-ttu-id="ea29a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea29a-119">-DefaultProfile</span></span>
<span data-ttu-id="ea29a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea29a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea29a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea29a-121">-Name</span></span>
<span data-ttu-id="ea29a-122">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-122">The name of the host group.</span></span>

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

### <span data-ttu-id="ea29a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea29a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea29a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea29a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea29a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea29a-125">-ResourceId</span></span>
<span data-ttu-id="ea29a-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea29a-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="ea29a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea29a-127">CommonParameters</span></span>
<span data-ttu-id="ea29a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea29a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea29a-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea29a-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea29a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea29a-130">INPUTS</span></span>

### <span data-ttu-id="ea29a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea29a-131">System.String</span></span>

## <span data-ttu-id="ea29a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea29a-132">OUTPUTS</span></span>

### <span data-ttu-id="ea29a-133">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="ea29a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="ea29a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea29a-134">NOTES</span></span>

## <span data-ttu-id="ea29a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea29a-135">RELATED LINKS</span></span>

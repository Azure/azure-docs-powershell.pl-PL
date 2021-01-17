---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339913"
---
# <span data-ttu-id="aa32c-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="aa32c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa32c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa32c-103">Zapisuje zmodyfikowany IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="aa32c-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="aa32c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa32c-104">SYNTAX</span></span>

### <span data-ttu-id="aa32c-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa32c-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa32c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa32c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa32c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa32c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa32c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa32c-108">DESCRIPTION</span></span>
<span data-ttu-id="aa32c-109">Polecenie cmdlet **Set-AzIpAllocation** aktualizuje platformę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="aa32c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa32c-110">EXAMPLES</span></span>

### <span data-ttu-id="aa32c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa32c-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="aa32c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa32c-112">PARAMETERS</span></span>

### <span data-ttu-id="aa32c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa32c-113">-AsJob</span></span>
<span data-ttu-id="aa32c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="aa32c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa32c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa32c-115">-DefaultProfile</span></span>
<span data-ttu-id="aa32c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa32c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa32c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa32c-117">-InputObject</span></span>
<span data-ttu-id="aa32c-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="aa32c-119">-IpAllocationTag</span></span>
<span data-ttu-id="aa32c-120">Znaczniki przydziału dla przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="aa32c-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa32c-121">-Name</span></span>
<span data-ttu-id="aa32c-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa32c-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa32c-123">-ResourceGroupName</span></span>
<span data-ttu-id="aa32c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa32c-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa32c-125">-ResourceId</span></span>
<span data-ttu-id="aa32c-126">Identyfikator IpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa32c-127">-Tag</span></span>
<span data-ttu-id="aa32c-128">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa32c-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa32c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa32c-129">CommonParameters</span></span>
<span data-ttu-id="aa32c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa32c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa32c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa32c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa32c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa32c-132">INPUTS</span></span>

### <span data-ttu-id="aa32c-133">Microsoft. Azure. Commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="aa32c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa32c-134">OUTPUTS</span></span>

### <span data-ttu-id="aa32c-135">Microsoft. Azure. Commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="aa32c-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="aa32c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa32c-136">NOTES</span></span>

## <span data-ttu-id="aa32c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa32c-137">RELATED LINKS</span></span>

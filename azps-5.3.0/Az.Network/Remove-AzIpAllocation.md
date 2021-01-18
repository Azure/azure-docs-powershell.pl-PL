---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500302"
---
# <span data-ttu-id="97f30-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="97f30-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="97f30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97f30-102">SYNOPSIS</span></span>
<span data-ttu-id="97f30-103">Usuwa usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="97f30-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="97f30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97f30-104">SYNTAX</span></span>

### <span data-ttu-id="97f30-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f30-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f30-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f30-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f30-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f30-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f30-108">Opis</span><span class="sxs-lookup"><span data-stu-id="97f30-108">DESCRIPTION</span></span>
<span data-ttu-id="97f30-109">Polecenie cmdlet **Remove-AzIpAllocation** usuwa składnik Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="97f30-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="97f30-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97f30-110">EXAMPLES</span></span>

### <span data-ttu-id="97f30-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97f30-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="97f30-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97f30-112">PARAMETERS</span></span>

### <span data-ttu-id="97f30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97f30-113">-AsJob</span></span>
<span data-ttu-id="97f30-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="97f30-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97f30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f30-115">-DefaultProfile</span></span>
<span data-ttu-id="97f30-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97f30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97f30-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97f30-117">-Force</span></span>
<span data-ttu-id="97f30-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97f30-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="97f30-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97f30-119">-InputObject</span></span>
<span data-ttu-id="97f30-120">{{Fillobject opis}}</span><span class="sxs-lookup"><span data-stu-id="97f30-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97f30-121">-Name</span></span>
<span data-ttu-id="97f30-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="97f30-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97f30-123">-PassThru</span></span>
<span data-ttu-id="97f30-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="97f30-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97f30-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="97f30-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97f30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f30-126">-ResourceGroupName</span></span>
<span data-ttu-id="97f30-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97f30-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97f30-128">-ResourceId</span></span>
<span data-ttu-id="97f30-129">Identyfikator zasobu IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="97f30-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97f30-130">-Confirm</span></span>
<span data-ttu-id="97f30-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f30-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f30-132">-WhatIf</span></span>
<span data-ttu-id="97f30-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97f30-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97f30-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f30-135">CommonParameters</span></span>
<span data-ttu-id="97f30-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f30-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97f30-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f30-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97f30-138">INPUTS</span></span>

### <span data-ttu-id="97f30-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97f30-139">System.String</span></span>

## <span data-ttu-id="97f30-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97f30-140">OUTPUTS</span></span>

### <span data-ttu-id="97f30-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97f30-141">System.Boolean</span></span>

## <span data-ttu-id="97f30-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97f30-142">NOTES</span></span>

## <span data-ttu-id="97f30-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97f30-143">RELATED LINKS</span></span>

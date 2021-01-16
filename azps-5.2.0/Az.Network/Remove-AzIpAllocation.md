---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363470"
---
# <span data-ttu-id="71e58-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="71e58-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="71e58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71e58-102">SYNOPSIS</span></span>
<span data-ttu-id="71e58-103">Usuwa usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="71e58-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="71e58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71e58-104">SYNTAX</span></span>

### <span data-ttu-id="71e58-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e58-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e58-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e58-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e58-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71e58-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e58-108">Opis</span><span class="sxs-lookup"><span data-stu-id="71e58-108">DESCRIPTION</span></span>
<span data-ttu-id="71e58-109">Polecenie cmdlet **Remove-AzIpAllocation** usuwa składnik Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="71e58-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="71e58-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71e58-110">EXAMPLES</span></span>

### <span data-ttu-id="71e58-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71e58-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="71e58-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71e58-112">PARAMETERS</span></span>

### <span data-ttu-id="71e58-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71e58-113">-AsJob</span></span>
<span data-ttu-id="71e58-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="71e58-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71e58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e58-115">-DefaultProfile</span></span>
<span data-ttu-id="71e58-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71e58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e58-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71e58-117">-Force</span></span>
<span data-ttu-id="71e58-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71e58-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="71e58-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71e58-119">-InputObject</span></span>
<span data-ttu-id="71e58-120">{{Fillobject opis}}</span><span class="sxs-lookup"><span data-stu-id="71e58-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="71e58-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71e58-121">-Name</span></span>
<span data-ttu-id="71e58-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="71e58-122">The resource name.</span></span>

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

### <span data-ttu-id="71e58-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71e58-123">-PassThru</span></span>
<span data-ttu-id="71e58-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="71e58-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71e58-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="71e58-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71e58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e58-126">-ResourceGroupName</span></span>
<span data-ttu-id="71e58-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71e58-127">The resource group name.</span></span>

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

### <span data-ttu-id="71e58-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71e58-128">-ResourceId</span></span>
<span data-ttu-id="71e58-129">Identyfikator zasobu IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="71e58-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="71e58-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71e58-130">-Confirm</span></span>
<span data-ttu-id="71e58-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e58-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e58-132">-WhatIf</span></span>
<span data-ttu-id="71e58-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e58-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71e58-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e58-135">CommonParameters</span></span>
<span data-ttu-id="71e58-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e58-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e58-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e58-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e58-138">INPUTS</span></span>

### <span data-ttu-id="71e58-139">System. String</span><span class="sxs-lookup"><span data-stu-id="71e58-139">System.String</span></span>

## <span data-ttu-id="71e58-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71e58-140">OUTPUTS</span></span>

### <span data-ttu-id="71e58-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71e58-141">System.Boolean</span></span>

## <span data-ttu-id="71e58-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71e58-142">NOTES</span></span>

## <span data-ttu-id="71e58-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e58-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: f3072871caa5449606afe18093a463fea58c6dfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976625"
---
# <span data-ttu-id="8c5c3-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="8c5c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5c3-103">Usuwa publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="8c5c3-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="8c5c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c5c3-104">SYNTAX</span></span>

### <span data-ttu-id="8c5c3-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c5c3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5c3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5c3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5c3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5c3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c5c3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-108">DESCRIPTION</span></span>
<span data-ttu-id="8c5c3-109">Polecenie **cmdlet Remove-AzPublicIpPrefix** usuwa publiczny prefiks IP platformy Azure, o ile nie są z niego przydzielone żadne publiczne adresy IP.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="8c5c3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c5c3-110">EXAMPLES</span></span>

### <span data-ttu-id="8c5c3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c5c3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="8c5c3-112">Usuwa publiczny prefiks IP z nazwami $prefixName grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="8c5c3-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="8c5c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-113">PARAMETERS</span></span>

### <span data-ttu-id="8c5c3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8c5c3-114">-AsJob</span></span>
<span data-ttu-id="8c5c3-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8c5c3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c5c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c3-116">-DefaultProfile</span></span>
<span data-ttu-id="8c5c3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c5c3-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8c5c3-118">-Force</span></span>
<span data-ttu-id="8c5c3-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8c5c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5c3-120">-InputObject</span></span>
<span data-ttu-id="8c5c3-121">Obiekt PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c5c3-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c5c3-122">-Name</span></span>
<span data-ttu-id="8c5c3-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c5c3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c5c3-124">-PassThru</span></span>
<span data-ttu-id="8c5c3-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c5c3-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c5c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c5c3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c5c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c3-129">-ResourceId</span></span>
<span data-ttu-id="8c5c3-130">ZasóbId zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8c5c3-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="8c5c3-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c5c3-131">-Confirm</span></span>
<span data-ttu-id="8c5c3-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c5c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5c3-133">-WhatIf</span></span>
<span data-ttu-id="8c5c3-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c5c3-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c5c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5c3-136">CommonParameters</span></span>
<span data-ttu-id="8c5c3-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5c3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5c3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5c3-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c5c3-139">INPUTS</span></span>

### <span data-ttu-id="8c5c3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c5c3-140">System.String</span></span>

### <span data-ttu-id="8c5c3-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="8c5c3-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c5c3-142">OUTPUTS</span></span>

### <span data-ttu-id="8c5c3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c5c3-143">System.Boolean</span></span>

## <span data-ttu-id="8c5c3-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c5c3-144">NOTES</span></span>

## <span data-ttu-id="8c5c3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c5c3-145">RELATED LINKS</span></span>

[<span data-ttu-id="8c5c3-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="8c5c3-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="8c5c3-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8c5c3-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)

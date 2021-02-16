---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186939"
---
# <span data-ttu-id="d7a41-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="d7a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7a41-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a41-103">Usuwa publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="d7a41-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="d7a41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7a41-104">SYNTAX</span></span>

### <span data-ttu-id="d7a41-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d7a41-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a41-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7a41-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a41-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7a41-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a41-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7a41-108">DESCRIPTION</span></span>
<span data-ttu-id="d7a41-109">Polecenie **cmdlet Remove-AzPublicIpPrefix** usuwa publiczny prefiks IP platformy Azure, o ile nie są z niego przydzielone żadne publiczne adresy IP.</span><span class="sxs-lookup"><span data-stu-id="d7a41-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="d7a41-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7a41-110">EXAMPLES</span></span>

### <span data-ttu-id="d7a41-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7a41-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="d7a41-112">Usuwa publiczny prefiks IP z nazwami $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="d7a41-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="d7a41-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7a41-113">PARAMETERS</span></span>

### <span data-ttu-id="d7a41-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d7a41-114">-AsJob</span></span>
<span data-ttu-id="d7a41-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7a41-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7a41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a41-116">-DefaultProfile</span></span>
<span data-ttu-id="d7a41-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a41-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d7a41-118">-Force</span></span>
<span data-ttu-id="d7a41-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7a41-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d7a41-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7a41-120">-InputObject</span></span>
<span data-ttu-id="d7a41-121">Obiekt PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="d7a41-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7a41-122">-Name</span></span>
<span data-ttu-id="d7a41-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d7a41-123">The resource name.</span></span>

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

### <span data-ttu-id="d7a41-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7a41-124">-PassThru</span></span>
<span data-ttu-id="d7a41-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d7a41-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7a41-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d7a41-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7a41-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a41-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7a41-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7a41-128">The resource group name.</span></span>

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

### <span data-ttu-id="d7a41-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7a41-129">-ResourceId</span></span>
<span data-ttu-id="d7a41-130">ZasóbId zasobu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d7a41-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="d7a41-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7a41-131">-Confirm</span></span>
<span data-ttu-id="d7a41-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7a41-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a41-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a41-133">-WhatIf</span></span>
<span data-ttu-id="d7a41-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a41-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a41-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d7a41-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a41-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a41-136">CommonParameters</span></span>
<span data-ttu-id="d7a41-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a41-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a41-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a41-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a41-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7a41-139">INPUTS</span></span>

### <span data-ttu-id="d7a41-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d7a41-140">System.String</span></span>

### <span data-ttu-id="d7a41-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="d7a41-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7a41-142">OUTPUTS</span></span>

### <span data-ttu-id="d7a41-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7a41-143">System.Boolean</span></span>

## <span data-ttu-id="d7a41-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7a41-144">NOTES</span></span>

## <span data-ttu-id="d7a41-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7a41-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7a41-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="d7a41-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="d7a41-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7a41-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)

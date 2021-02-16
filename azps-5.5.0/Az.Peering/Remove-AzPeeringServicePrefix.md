---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184026"
---
# <span data-ttu-id="df6cd-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="df6cd-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="df6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="df6cd-103">Usuwa prefiks nowej usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="df6cd-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="df6cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df6cd-104">SYNTAX</span></span>

### <span data-ttu-id="df6cd-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="df6cd-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df6cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df6cd-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df6cd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df6cd-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df6cd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="df6cd-108">DESCRIPTION</span></span>
<span data-ttu-id="df6cd-109">Usuwa prefiks usługi komunikacji równorzędnej z usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="df6cd-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="df6cd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df6cd-110">EXAMPLES</span></span>

### <span data-ttu-id="df6cd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df6cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="df6cd-112">Usuwanie prefiksu z obiektu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="df6cd-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="df6cd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="df6cd-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="df6cd-114">Usuwanie prefiksu z identyfikatora zasobu usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="df6cd-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="df6cd-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="df6cd-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="df6cd-116">Usuwanie prefiksu z nazwy i nazwy grupy zasobów usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="df6cd-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="df6cd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df6cd-117">PARAMETERS</span></span>

### <span data-ttu-id="df6cd-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="df6cd-118">-AsJob</span></span>
<span data-ttu-id="df6cd-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="df6cd-119">Run in the background.</span></span>

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

### <span data-ttu-id="df6cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6cd-120">-DefaultProfile</span></span>
<span data-ttu-id="df6cd-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df6cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df6cd-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="df6cd-122">-Force</span></span>
<span data-ttu-id="df6cd-123">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="df6cd-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="df6cd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df6cd-124">-InputObject</span></span>
<span data-ttu-id="df6cd-125">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="df6cd-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df6cd-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="df6cd-126">-Name</span></span>
<span data-ttu-id="df6cd-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="df6cd-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6cd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df6cd-128">-PassThru</span></span>
<span data-ttu-id="df6cd-129">Zwraca wartość prawda dla sukcesu lub fałsz dla błędu.</span><span class="sxs-lookup"><span data-stu-id="df6cd-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="df6cd-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="df6cd-130">-PrefixName</span></span>
<span data-ttu-id="df6cd-131">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="df6cd-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="df6cd-133">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df6cd-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6cd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df6cd-134">-ResourceId</span></span>
<span data-ttu-id="df6cd-135">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="df6cd-135">The resource id string name.</span></span>

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

### <span data-ttu-id="df6cd-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df6cd-136">-Confirm</span></span>
<span data-ttu-id="df6cd-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="df6cd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df6cd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6cd-138">-WhatIf</span></span>
<span data-ttu-id="df6cd-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df6cd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6cd-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="df6cd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df6cd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6cd-141">CommonParameters</span></span>
<span data-ttu-id="df6cd-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6cd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6cd-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df6cd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6cd-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df6cd-144">INPUTS</span></span>

### <span data-ttu-id="df6cd-145">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="df6cd-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="df6cd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="df6cd-146">System.String</span></span>

## <span data-ttu-id="df6cd-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df6cd-147">OUTPUTS</span></span>

### <span data-ttu-id="df6cd-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df6cd-148">System.Boolean</span></span>

## <span data-ttu-id="df6cd-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df6cd-149">NOTES</span></span>

## <span data-ttu-id="df6cd-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df6cd-150">RELATED LINKS</span></span>

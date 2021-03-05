---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 3922492f4d72886e0608108811906387e31472b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989297"
---
# <span data-ttu-id="7eb4b-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7eb4b-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="7eb4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb4b-103">Usuwa prefiks nowej usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="7eb4b-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="7eb4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7eb4b-104">SYNTAX</span></span>

### <span data-ttu-id="7eb4b-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="7eb4b-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb4b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb4b-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb4b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb4b-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb4b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7eb4b-108">DESCRIPTION</span></span>
<span data-ttu-id="7eb4b-109">Usuwa prefiks usługi komunikacji równorzędnej z usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="7eb4b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7eb4b-110">EXAMPLES</span></span>

### <span data-ttu-id="7eb4b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7eb4b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="7eb4b-112">Usuwanie prefiksu z obiektu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="7eb4b-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="7eb4b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7eb4b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="7eb4b-114">Usuwanie prefiksu z identyfikatora zasobu usługi komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="7eb4b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7eb4b-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="7eb4b-116">Usuwanie prefiksu z nazwy i nazwy grupy zasobów usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="7eb4b-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="7eb4b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eb4b-117">PARAMETERS</span></span>

### <span data-ttu-id="7eb4b-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7eb4b-118">-AsJob</span></span>
<span data-ttu-id="7eb4b-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-119">Run in the background.</span></span>

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

### <span data-ttu-id="7eb4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb4b-120">-DefaultProfile</span></span>
<span data-ttu-id="7eb4b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb4b-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7eb4b-122">-Force</span></span>
<span data-ttu-id="7eb4b-123">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="7eb4b-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="7eb4b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb4b-124">-InputObject</span></span>
<span data-ttu-id="7eb4b-125">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7eb4b-125">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="7eb4b-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7eb4b-126">-Name</span></span>
<span data-ttu-id="7eb4b-127">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7eb4b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eb4b-128">-PassThru</span></span>
<span data-ttu-id="7eb4b-129">Zwraca wartość prawda dla sukcesu lub fałsz dla błędu.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="7eb4b-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="7eb4b-130">-PrefixName</span></span>
<span data-ttu-id="7eb4b-131">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-131">The name of prefix.</span></span>

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

### <span data-ttu-id="7eb4b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb4b-132">-ResourceGroupName</span></span>
<span data-ttu-id="7eb4b-133">Tworzenie lub używanie nazwy istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7eb4b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb4b-134">-ResourceId</span></span>
<span data-ttu-id="7eb4b-135">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-135">The resource id string name.</span></span>

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

### <span data-ttu-id="7eb4b-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7eb4b-136">-Confirm</span></span>
<span data-ttu-id="7eb4b-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb4b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb4b-138">-WhatIf</span></span>
<span data-ttu-id="7eb4b-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb4b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb4b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb4b-141">CommonParameters</span></span>
<span data-ttu-id="7eb4b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb4b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb4b-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eb4b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb4b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb4b-144">INPUTS</span></span>

### <span data-ttu-id="7eb4b-145">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7eb4b-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="7eb4b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7eb4b-146">System.String</span></span>

## <span data-ttu-id="7eb4b-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb4b-147">OUTPUTS</span></span>

### <span data-ttu-id="7eb4b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7eb4b-148">System.Boolean</span></span>

## <span data-ttu-id="7eb4b-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7eb4b-149">NOTES</span></span>

## <span data-ttu-id="7eb4b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb4b-150">RELATED LINKS</span></span>

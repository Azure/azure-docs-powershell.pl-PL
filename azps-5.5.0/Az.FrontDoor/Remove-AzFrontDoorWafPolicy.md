---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185915"
---
# <span data-ttu-id="3e179-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="3e179-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="3e179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e179-102">SYNOPSIS</span></span>
<span data-ttu-id="3e179-103">Usuwanie zasad SAF</span><span class="sxs-lookup"><span data-stu-id="3e179-103">Remove WAF policy</span></span>

## <span data-ttu-id="3e179-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e179-104">SYNTAX</span></span>

### <span data-ttu-id="3e179-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3e179-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e179-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e179-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e179-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e179-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e179-108">DESCRIPTION</span></span>
<span data-ttu-id="3e179-109">Polecenie **cmdlet Remove-AzFrontDoorWafPolicy** usuwa zasady WAF w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e179-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="3e179-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e179-110">EXAMPLES</span></span>

### <span data-ttu-id="3e179-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e179-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="3e179-112">Usuń zasady SAF nazywane $policyName w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3e179-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="3e179-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e179-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="3e179-114">Usuń wszystkie zasady SAF w $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3e179-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="3e179-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e179-115">PARAMETERS</span></span>

### <span data-ttu-id="3e179-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e179-116">-DefaultProfile</span></span>
<span data-ttu-id="3e179-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e179-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e179-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e179-118">-InputObject</span></span>
<span data-ttu-id="3e179-119">Obiekt zasad SAF do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3e179-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e179-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3e179-120">-Name</span></span>
<span data-ttu-id="3e179-121">Nazwa zasad SAF do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3e179-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e179-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e179-122">-PassThru</span></span>
<span data-ttu-id="3e179-123">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="3e179-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="3e179-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e179-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e179-125">Grupa zasobów, do której należą zasady SAF.</span><span class="sxs-lookup"><span data-stu-id="3e179-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e179-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e179-126">-ResourceId</span></span>
<span data-ttu-id="3e179-127">Identyfikator zasobu zasad SAF do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3e179-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e179-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e179-128">-Confirm</span></span>
<span data-ttu-id="3e179-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e179-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e179-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e179-130">-WhatIf</span></span>
<span data-ttu-id="3e179-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e179-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e179-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e179-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e179-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e179-133">CommonParameters</span></span>
<span data-ttu-id="3e179-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e179-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e179-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e179-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e179-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e179-136">INPUTS</span></span>

### <span data-ttu-id="3e179-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="3e179-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="3e179-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3e179-138">System.String</span></span>

## <span data-ttu-id="3e179-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e179-139">OUTPUTS</span></span>

### <span data-ttu-id="3e179-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e179-140">System.Boolean</span></span>

## <span data-ttu-id="3e179-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e179-141">NOTES</span></span>

## <span data-ttu-id="3e179-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e179-142">RELATED LINKS</span></span>

<span data-ttu-id="3e179-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3e179-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>

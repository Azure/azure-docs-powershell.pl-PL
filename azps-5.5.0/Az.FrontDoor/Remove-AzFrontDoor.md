---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185930"
---
# <span data-ttu-id="d69d7-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d69d7-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="d69d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d69d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d69d7-103">Usuwanie równoważenia obciążenia drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="d69d7-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="d69d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d69d7-104">SYNTAX</span></span>

### <span data-ttu-id="d69d7-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d69d7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69d7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d69d7-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69d7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d69d7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69d7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d69d7-108">DESCRIPTION</span></span>
<span data-ttu-id="d69d7-109">Polecenie **cmdlet Remove-AzFrontDoor** usuwa równoważenie obciążenia drzwi frontowych w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d69d7-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="d69d7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d69d7-110">EXAMPLES</span></span>

### <span data-ttu-id="d69d7-111">Przykład 1. Usunięcie ciągu "frontdoor1" w grupie zasobów "rg1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="d69d7-112">Usuń "frontdoor1" z grupy zasobów "rg1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="d69d7-113">Przykład 2. Usuwanie wszystkich frontoorów w grupie zasobów "rg1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="d69d7-114">Usuń wszystkie frontoory z grupy zasobów "rg1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="d69d7-115">Przykład 3. Usunięcie wszystkich frontdoorów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="d69d7-116">Usuń wszystkie frontory w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="d69d7-117">Przykład 4. Usuń wszystkie frontdoory z nazwą "frontdoor1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="d69d7-118">Usuń wszystkie frontdoory z nazwą "frontdoor1" w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d69d7-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="d69d7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d69d7-119">PARAMETERS</span></span>

### <span data-ttu-id="d69d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69d7-120">-DefaultProfile</span></span>
<span data-ttu-id="d69d7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d69d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d69d7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d69d7-122">-InputObject</span></span>
<span data-ttu-id="d69d7-123">Obiekt Drzwi przednie do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d69d7-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d69d7-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d69d7-124">-Name</span></span>
<span data-ttu-id="d69d7-125">Nazwa drzwi frontowych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d69d7-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="d69d7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d69d7-126">-PassThru</span></span>
<span data-ttu-id="d69d7-127">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="d69d7-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="d69d7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69d7-128">-ResourceGroupName</span></span>
<span data-ttu-id="d69d7-129">Grupa zasobów, do której należy drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="d69d7-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="d69d7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d69d7-130">-ResourceId</span></span>
<span data-ttu-id="d69d7-131">Identyfikator zasobu drzwi frontowych do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d69d7-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="d69d7-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d69d7-132">-Confirm</span></span>
<span data-ttu-id="d69d7-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d69d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69d7-134">-WhatIf</span></span>
<span data-ttu-id="d69d7-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d69d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69d7-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d69d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69d7-137">CommonParameters</span></span>
<span data-ttu-id="d69d7-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69d7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d69d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69d7-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d69d7-140">INPUTS</span></span>

### <span data-ttu-id="d69d7-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d69d7-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="d69d7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d69d7-142">System.String</span></span>

## <span data-ttu-id="d69d7-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d69d7-143">OUTPUTS</span></span>

### <span data-ttu-id="d69d7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d69d7-144">System.Boolean</span></span>

## <span data-ttu-id="d69d7-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d69d7-145">NOTES</span></span>

## <span data-ttu-id="d69d7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d69d7-146">RELATED LINKS</span></span>

<span data-ttu-id="d69d7-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d69d7-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>
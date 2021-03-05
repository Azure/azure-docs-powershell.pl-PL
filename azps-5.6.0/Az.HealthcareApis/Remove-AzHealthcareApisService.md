---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 448b400d4a01924d7ef2ce64acc0f7edf827b827
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013169"
---
# <span data-ttu-id="c8b0c-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="c8b0c-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="c8b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b0c-103">Usuwa wystąpienie usługi.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-103">Deletes a service instance.</span></span>

## <span data-ttu-id="c8b0c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8b0c-104">SYNTAX</span></span>

### <span data-ttu-id="c8b0c-105">ServiceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c8b0c-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b0c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8b0c-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b0c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8b0c-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8b0c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8b0c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8b0c-109">Usuwa wystąpienie usługi.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-109">Deletes a service instance.</span></span>

## <span data-ttu-id="c8b0c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8b0c-110">EXAMPLES</span></span>

### <span data-ttu-id="c8b0c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8b0c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="c8b0c-112">Usuwa istniejącą usługę HealthcareApis z podaną nazwą w obrębie podanej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="c8b0c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c8b0c-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="c8b0c-114">Usuwa istniejącą usługę HealthcareApis z podaną grupę ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="c8b0c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c8b0c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="c8b0c-116">Usuwa dostarczony obiekt usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="c8b0c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8b0c-117">PARAMETERS</span></span>

### <span data-ttu-id="c8b0c-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c8b0c-118">-AsJob</span></span>
<span data-ttu-id="c8b0c-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="c8b0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b0c-120">-DefaultProfile</span></span>
<span data-ttu-id="c8b0c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8b0c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8b0c-122">-InputObject</span></span>
<span data-ttu-id="c8b0c-123">Obiekt usługi HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="c8b0c-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b0c-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c8b0c-124">-Name</span></span>
<span data-ttu-id="c8b0c-125">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b0c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8b0c-126">-PassThru</span></span>
<span data-ttu-id="c8b0c-127">Jeśli zostanie podany, zwraca wartość prawda, jeśli operacja się powiedzie</span><span class="sxs-lookup"><span data-stu-id="c8b0c-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="c8b0c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b0c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c8b0c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b0c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8b0c-130">-ResourceId</span></span>
<span data-ttu-id="c8b0c-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b0c-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8b0c-132">-Confirm</span></span>
<span data-ttu-id="c8b0c-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8b0c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8b0c-134">-WhatIf</span></span>
<span data-ttu-id="c8b0c-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8b0c-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8b0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b0c-137">CommonParameters</span></span>
<span data-ttu-id="c8b0c-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b0c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8b0c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b0c-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8b0c-140">INPUTS</span></span>

### <span data-ttu-id="c8b0c-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="c8b0c-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="c8b0c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c8b0c-142">System.String</span></span>

## <span data-ttu-id="c8b0c-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8b0c-143">OUTPUTS</span></span>

### <span data-ttu-id="c8b0c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8b0c-144">System.Boolean</span></span>

## <span data-ttu-id="c8b0c-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8b0c-145">NOTES</span></span>

## <span data-ttu-id="c8b0c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8b0c-146">RELATED LINKS</span></span>

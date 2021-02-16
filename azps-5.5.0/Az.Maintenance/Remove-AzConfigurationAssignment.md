---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180338"
---
# <span data-ttu-id="e7b6a-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e7b6a-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="e7b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b6a-103">Wyrejestruj konfigurację dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e7b6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7b6a-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7b6a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b6a-106">Wyrejestruj konfigurację dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e7b6a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="e7b6a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7b6a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="e7b6a-109">Wyrejestruj konfigurację zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e7b6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7b6a-110">PARAMETERS</span></span>

### <span data-ttu-id="e7b6a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e7b6a-111">-AsJob</span></span>
<span data-ttu-id="e7b6a-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e7b6a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7b6a-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e7b6a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="e7b6a-114">Nazwa zadania konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-114">The configuration assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b6a-115">-DefaultProfile</span></span>
<span data-ttu-id="e7b6a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7b6a-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e7b6a-117">-Force</span></span>
<span data-ttu-id="e7b6a-118">Wymusz usunięcie bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="e7b6a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7b6a-119">-PassThru</span></span>
<span data-ttu-id="e7b6a-120">Zwraca stan operacji Usuń.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e7b6a-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7b6a-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e7b6a-122">-ProviderName</span></span>
<span data-ttu-id="e7b6a-123">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7b6a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e7b6a-126">-ResourceName</span></span>
<span data-ttu-id="e7b6a-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e7b6a-128">-ResourceParentName</span></span>
<span data-ttu-id="e7b6a-129">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e7b6a-130">-ResourceParentType</span></span>
<span data-ttu-id="e7b6a-131">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e7b6a-132">-ResourceType</span></span>
<span data-ttu-id="e7b6a-133">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b6a-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7b6a-134">-Confirm</span></span>
<span data-ttu-id="e7b6a-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b6a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b6a-136">-WhatIf</span></span>
<span data-ttu-id="e7b6a-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b6a-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b6a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b6a-139">CommonParameters</span></span>
<span data-ttu-id="e7b6a-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b6a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b6a-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7b6a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b6a-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7b6a-142">INPUTS</span></span>

### <span data-ttu-id="e7b6a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e7b6a-143">System.String</span></span>

## <span data-ttu-id="e7b6a-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7b6a-144">OUTPUTS</span></span>

### <span data-ttu-id="e7b6a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7b6a-145">System.Boolean</span></span>

## <span data-ttu-id="e7b6a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7b6a-146">NOTES</span></span>

## <span data-ttu-id="e7b6a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7b6a-147">RELATED LINKS</span></span>

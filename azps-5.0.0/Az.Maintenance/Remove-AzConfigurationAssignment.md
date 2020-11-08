---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231821"
---
# <span data-ttu-id="a0fdd-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a0fdd-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="a0fdd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fdd-103">Wyrejestrowanie konfiguracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="a0fdd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0fdd-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0fdd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fdd-106">Wyrejestrowanie konfiguracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="a0fdd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="a0fdd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0fdd-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="a0fdd-109">Wyrejestrowanie konfiguracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="a0fdd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="a0fdd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0fdd-111">-AsJob</span></span>
<span data-ttu-id="a0fdd-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a0fdd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0fdd-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a0fdd-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="a0fdd-114">Nazwa przydziału konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="a0fdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fdd-115">-DefaultProfile</span></span>
<span data-ttu-id="a0fdd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0fdd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0fdd-117">-Force</span></span>
<span data-ttu-id="a0fdd-118">Wymuszaj usunięcie bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="a0fdd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0fdd-119">-PassThru</span></span>
<span data-ttu-id="a0fdd-120">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a0fdd-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0fdd-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="a0fdd-122">-ProviderName</span></span>
<span data-ttu-id="a0fdd-123">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="a0fdd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fdd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0fdd-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="a0fdd-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a0fdd-126">-ResourceName</span></span>
<span data-ttu-id="a0fdd-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-127">The resource name.</span></span>

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

### <span data-ttu-id="a0fdd-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="a0fdd-128">-ResourceParentName</span></span>
<span data-ttu-id="a0fdd-129">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-129">The parent resource name.</span></span>

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

### <span data-ttu-id="a0fdd-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="a0fdd-130">-ResourceParentType</span></span>
<span data-ttu-id="a0fdd-131">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-131">The parent resource type.</span></span>

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

### <span data-ttu-id="a0fdd-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a0fdd-132">-ResourceType</span></span>
<span data-ttu-id="a0fdd-133">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-133">The resource type.</span></span>

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

### <span data-ttu-id="a0fdd-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0fdd-134">-Confirm</span></span>
<span data-ttu-id="a0fdd-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0fdd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0fdd-136">-WhatIf</span></span>
<span data-ttu-id="a0fdd-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0fdd-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0fdd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fdd-139">CommonParameters</span></span>
<span data-ttu-id="a0fdd-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fdd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fdd-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0fdd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fdd-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0fdd-142">INPUTS</span></span>

### <span data-ttu-id="a0fdd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a0fdd-143">System.String</span></span>

## <span data-ttu-id="a0fdd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0fdd-144">OUTPUTS</span></span>

### <span data-ttu-id="a0fdd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0fdd-145">System.Boolean</span></span>

## <span data-ttu-id="a0fdd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0fdd-146">NOTES</span></span>

## <span data-ttu-id="a0fdd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0fdd-147">RELATED LINKS</span></span>

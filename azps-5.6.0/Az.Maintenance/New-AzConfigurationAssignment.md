---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 993c1968d144a5a1a56a0bd3dff46a9920a90264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012913"
---
# <span data-ttu-id="bbd56-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="bbd56-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="bbd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd56-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd56-103">Zarejestruj konfigurację dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-103">Register configuration for resource.</span></span>

## <span data-ttu-id="bbd56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bbd56-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbd56-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bbd56-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd56-106">Zarejestruj konfigurację konserwacji zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="bbd56-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bbd56-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd56-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bbd56-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="bbd56-109">Zarejestruj konfigurację konserwacji hosta dedykowanego.</span><span class="sxs-lookup"><span data-stu-id="bbd56-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="bbd56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd56-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd56-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bbd56-111">-AsJob</span></span>
<span data-ttu-id="bbd56-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bbd56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbd56-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="bbd56-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="bbd56-114">Nazwa zadania konfiguracji powinna być zgodne z parametrem MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="bbd56-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="bbd56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd56-115">-DefaultProfile</span></span>
<span data-ttu-id="bbd56-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd56-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bbd56-117">-Location</span></span>
<span data-ttu-id="bbd56-118">Lokalizacja bez spacji dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd56-119">- MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bbd56-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="bbd56-120">W pełni kwalifikowana konfiguracja MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bbd56-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd56-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="bbd56-121">-ProviderName</span></span>
<span data-ttu-id="bbd56-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bbd56-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="bbd56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd56-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbd56-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bbd56-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="bbd56-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd56-125">-ResourceId</span></span>
<span data-ttu-id="bbd56-126">Nazwa zadania konfiguracji powinna być zgodne z parametrem MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="bbd56-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd56-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bbd56-127">-ResourceName</span></span>
<span data-ttu-id="bbd56-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-128">The resource name.</span></span>

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

### <span data-ttu-id="bbd56-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="bbd56-129">-ResourceParentName</span></span>
<span data-ttu-id="bbd56-130">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="bbd56-130">The parent resource name.</span></span>

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

### <span data-ttu-id="bbd56-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="bbd56-131">-ResourceParentType</span></span>
<span data-ttu-id="bbd56-132">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-132">The parent resource type.</span></span>

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

### <span data-ttu-id="bbd56-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bbd56-133">-ResourceType</span></span>
<span data-ttu-id="bbd56-134">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="bbd56-134">The resource type.</span></span>

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

### <span data-ttu-id="bbd56-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbd56-135">-Confirm</span></span>
<span data-ttu-id="bbd56-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bbd56-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd56-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd56-137">-WhatIf</span></span>
<span data-ttu-id="bbd56-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd56-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd56-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bbd56-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd56-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd56-140">CommonParameters</span></span>
<span data-ttu-id="bbd56-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd56-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd56-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbd56-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd56-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbd56-143">INPUTS</span></span>

### <span data-ttu-id="bbd56-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bbd56-144">System.String</span></span>

## <span data-ttu-id="bbd56-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbd56-145">OUTPUTS</span></span>

### <span data-ttu-id="bbd56-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="bbd56-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="bbd56-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bbd56-147">NOTES</span></span>

## <span data-ttu-id="bbd56-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbd56-148">RELATED LINKS</span></span>

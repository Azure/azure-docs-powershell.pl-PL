---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503313"
---
# <span data-ttu-id="d43c2-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="d43c2-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="d43c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d43c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d43c2-103">Rejestrowanie konfiguracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-103">Register configuration for resource.</span></span>

## <span data-ttu-id="d43c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d43c2-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d43c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d43c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d43c2-106">Rejestrowanie konfiguracji obsługi dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="d43c2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d43c2-107">EXAMPLES</span></span>

### <span data-ttu-id="d43c2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d43c2-108">Example 1</span></span>
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

<span data-ttu-id="d43c2-109">Rejestrowanie konfiguracji obsługi dla dedykowanego hosta.</span><span class="sxs-lookup"><span data-stu-id="d43c2-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="d43c2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d43c2-110">PARAMETERS</span></span>

### <span data-ttu-id="d43c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d43c2-111">-AsJob</span></span>
<span data-ttu-id="d43c2-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d43c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d43c2-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d43c2-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="d43c2-114">Nazwa przydziału konfiguracji powinna być zgodna z MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="d43c2-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="d43c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43c2-115">-DefaultProfile</span></span>
<span data-ttu-id="d43c2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d43c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43c2-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d43c2-117">-Location</span></span>
<span data-ttu-id="d43c2-118">Lokalizacja bez spacji dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="d43c2-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d43c2-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="d43c2-120">W pełni kwalifikowana MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d43c2-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="d43c2-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="d43c2-121">-ProviderName</span></span>
<span data-ttu-id="d43c2-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d43c2-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="d43c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="d43c2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d43c2-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="d43c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d43c2-125">-ResourceId</span></span>
<span data-ttu-id="d43c2-126">Nazwa przydziału konfiguracji powinna być zgodna z MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="d43c2-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="d43c2-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d43c2-127">-ResourceName</span></span>
<span data-ttu-id="d43c2-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-128">The resource name.</span></span>

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

### <span data-ttu-id="d43c2-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="d43c2-129">-ResourceParentName</span></span>
<span data-ttu-id="d43c2-130">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="d43c2-130">The parent resource name.</span></span>

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

### <span data-ttu-id="d43c2-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="d43c2-131">-ResourceParentType</span></span>
<span data-ttu-id="d43c2-132">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-132">The parent resource type.</span></span>

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

### <span data-ttu-id="d43c2-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d43c2-133">-ResourceType</span></span>
<span data-ttu-id="d43c2-134">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="d43c2-134">The resource type.</span></span>

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

### <span data-ttu-id="d43c2-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d43c2-135">-Confirm</span></span>
<span data-ttu-id="d43c2-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d43c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43c2-137">-WhatIf</span></span>
<span data-ttu-id="d43c2-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d43c2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d43c2-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d43c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43c2-140">CommonParameters</span></span>
<span data-ttu-id="d43c2-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43c2-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d43c2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43c2-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d43c2-143">INPUTS</span></span>

### <span data-ttu-id="d43c2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d43c2-144">System.String</span></span>

## <span data-ttu-id="d43c2-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d43c2-145">OUTPUTS</span></span>

### <span data-ttu-id="d43c2-146">Microsoft. Azure. Commands. Maintenance. models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="d43c2-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="d43c2-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d43c2-147">NOTES</span></span>

## <span data-ttu-id="d43c2-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d43c2-148">RELATED LINKS</span></span>

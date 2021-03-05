---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: ac264e048ea428ba68caa683eb6076074c9894b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985993"
---
# <span data-ttu-id="1fde3-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fde3-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="1fde3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fde3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fde3-103">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="1fde3-103">Create or Update configuration record</span></span>

## <span data-ttu-id="1fde3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1fde3-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fde3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1fde3-105">DESCRIPTION</span></span>
<span data-ttu-id="1fde3-106">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="1fde3-106">Create or Update configuration record</span></span>

## <span data-ttu-id="1fde3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1fde3-107">EXAMPLES</span></span>

### <span data-ttu-id="1fde3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fde3-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="1fde3-109">Tworzenie konfiguracji konserwacji za pomocą hosta zakresu</span><span class="sxs-lookup"><span data-stu-id="1fde3-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="1fde3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fde3-110">PARAMETERS</span></span>

### <span data-ttu-id="1fde3-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1fde3-111">-AsJob</span></span>
<span data-ttu-id="1fde3-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1fde3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fde3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fde3-113">-DefaultProfile</span></span>
<span data-ttu-id="1fde3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fde3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fde3-115">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="1fde3-115">-Duration</span></span>
<span data-ttu-id="1fde3-116">Czas trwania</span><span class="sxs-lookup"><span data-stu-id="1fde3-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fde3-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="1fde3-117">-ExpirationDateTime</span></span>
<span data-ttu-id="1fde3-118">Data wygaśnięciaDateGodziny harmonogramu w formacie YYYY-MM-DD gg:mm</span><span class="sxs-lookup"><span data-stu-id="1fde3-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="1fde3-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="1fde3-119">-ExtensionProperty</span></span>
<span data-ttu-id="1fde3-120">Właściwości rozszerzenia dla każdego zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fde3-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fde3-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1fde3-121">-Location</span></span>
<span data-ttu-id="1fde3-122">Lokalizacja konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="1fde3-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="1fde3-123">- MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="1fde3-123">-MaintenanceScope</span></span>
<span data-ttu-id="1fde3-124">Zakres konserwacji.</span><span class="sxs-lookup"><span data-stu-id="1fde3-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="1fde3-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1fde3-125">-Name</span></span>
<span data-ttu-id="1fde3-126">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="1fde3-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="1fde3-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="1fde3-127">-RecurEvery</span></span>
<span data-ttu-id="1fde3-128">Cykl harmonogramu</span><span class="sxs-lookup"><span data-stu-id="1fde3-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="1fde3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fde3-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fde3-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1fde3-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="1fde3-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="1fde3-131">-StartDateTime</span></span>
<span data-ttu-id="1fde3-132">Czas Rozpoczęcia harmonogramu w formacie YYYY-MM-DD gg:mm</span><span class="sxs-lookup"><span data-stu-id="1fde3-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="1fde3-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="1fde3-133">-Tag</span></span>
<span data-ttu-id="1fde3-134">Tagi ARM.</span><span class="sxs-lookup"><span data-stu-id="1fde3-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fde3-135">— strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="1fde3-135">-Timezone</span></span>
<span data-ttu-id="1fde3-136">Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="1fde3-136">The timezone</span></span>

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

### <span data-ttu-id="1fde3-137">— Widoczność</span><span class="sxs-lookup"><span data-stu-id="1fde3-137">-Visibility</span></span>
<span data-ttu-id="1fde3-138">Widoczność zakresu</span><span class="sxs-lookup"><span data-stu-id="1fde3-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="1fde3-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fde3-139">-Confirm</span></span>
<span data-ttu-id="1fde3-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1fde3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fde3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fde3-141">-WhatIf</span></span>
<span data-ttu-id="1fde3-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fde3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fde3-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1fde3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fde3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fde3-144">CommonParameters</span></span>
<span data-ttu-id="1fde3-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fde3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fde3-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fde3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fde3-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fde3-147">INPUTS</span></span>

### <span data-ttu-id="1fde3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1fde3-148">System.String</span></span>

## <span data-ttu-id="1fde3-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fde3-149">OUTPUTS</span></span>

### <span data-ttu-id="1fde3-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fde3-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="1fde3-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1fde3-151">NOTES</span></span>

## <span data-ttu-id="1fde3-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fde3-152">RELATED LINKS</span></span>

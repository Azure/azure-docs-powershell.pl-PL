---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232168"
---
# <span data-ttu-id="9b6dd-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b6dd-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="9b6dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6dd-103">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="9b6dd-103">Create or Update configuration record</span></span>

## <span data-ttu-id="9b6dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b6dd-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b6dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6dd-106">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="9b6dd-106">Create or Update configuration record</span></span>

## <span data-ttu-id="9b6dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6dd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b6dd-108">Example 1</span></span>
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

<span data-ttu-id="9b6dd-109">Tworzenie konfiguracji obsługi za pomocą hosta zakresu</span><span class="sxs-lookup"><span data-stu-id="9b6dd-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="9b6dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b6dd-110">PARAMETERS</span></span>

### <span data-ttu-id="9b6dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b6dd-111">-AsJob</span></span>
<span data-ttu-id="9b6dd-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b6dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b6dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6dd-113">-DefaultProfile</span></span>
<span data-ttu-id="9b6dd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b6dd-115">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="9b6dd-115">-Duration</span></span>
<span data-ttu-id="9b6dd-116">Czas trwania</span><span class="sxs-lookup"><span data-stu-id="9b6dd-116">The duration</span></span>


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

### <span data-ttu-id="9b6dd-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="9b6dd-117">-ExpirationDateTime</span></span>
<span data-ttu-id="9b6dd-118">ExpirationDateTime harmonogramu w formacie RRRR-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="9b6dd-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="9b6dd-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="9b6dd-119">-ExtensionProperty</span></span>
<span data-ttu-id="9b6dd-120">Właściwości rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="9b6dd-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9b6dd-121">-Location</span></span>
<span data-ttu-id="9b6dd-122">Lokalizacja konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="9b6dd-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="9b6dd-123">-MaintenanceScope</span></span>
<span data-ttu-id="9b6dd-124">Zakres konserwacji.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="9b6dd-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b6dd-125">-Name</span></span>
<span data-ttu-id="9b6dd-126">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="9b6dd-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="9b6dd-127">-RecurEvery</span></span>
<span data-ttu-id="9b6dd-128">Cykl harmonogramu</span><span class="sxs-lookup"><span data-stu-id="9b6dd-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="9b6dd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6dd-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b6dd-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="9b6dd-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="9b6dd-131">-StartDateTime</span></span>
<span data-ttu-id="9b6dd-132">StartDateTime harmonogramu w formacie RRRR-MM-DD hh: mm</span><span class="sxs-lookup"><span data-stu-id="9b6dd-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="9b6dd-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b6dd-133">-Tag</span></span>
<span data-ttu-id="9b6dd-134">Znaczniki ARM.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="9b6dd-135">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="9b6dd-135">-Timezone</span></span>
<span data-ttu-id="9b6dd-136">Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="9b6dd-136">The timezone</span></span>

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

### <span data-ttu-id="9b6dd-137">-Widoczność</span><span class="sxs-lookup"><span data-stu-id="9b6dd-137">-Visibility</span></span>
<span data-ttu-id="9b6dd-138">Widoczność zakresu</span><span class="sxs-lookup"><span data-stu-id="9b6dd-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="9b6dd-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b6dd-139">-Confirm</span></span>
<span data-ttu-id="9b6dd-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6dd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6dd-141">-WhatIf</span></span>
<span data-ttu-id="9b6dd-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6dd-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6dd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6dd-144">CommonParameters</span></span>
<span data-ttu-id="9b6dd-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6dd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6dd-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b6dd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6dd-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b6dd-147">INPUTS</span></span>

### <span data-ttu-id="9b6dd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6dd-148">System.String</span></span>

## <span data-ttu-id="9b6dd-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b6dd-149">OUTPUTS</span></span>

### <span data-ttu-id="9b6dd-150">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b6dd-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="9b6dd-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b6dd-151">NOTES</span></span>

## <span data-ttu-id="9b6dd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b6dd-152">RELATED LINKS</span></span>

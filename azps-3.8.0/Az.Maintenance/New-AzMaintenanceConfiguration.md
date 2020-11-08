---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053186"
---
# <span data-ttu-id="16484-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="16484-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="16484-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16484-102">SYNOPSIS</span></span>
<span data-ttu-id="16484-103">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="16484-103">Create or Update configuration record</span></span>

## <span data-ttu-id="16484-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16484-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16484-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16484-105">DESCRIPTION</span></span>
<span data-ttu-id="16484-106">Tworzenie lub aktualizowanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="16484-106">Create or Update configuration record</span></span>

## <span data-ttu-id="16484-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16484-107">EXAMPLES</span></span>

### <span data-ttu-id="16484-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16484-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="16484-109">Tworzenie konfiguracji obsługi za pomocą hosta zakresu</span><span class="sxs-lookup"><span data-stu-id="16484-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="16484-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16484-110">PARAMETERS</span></span>

### <span data-ttu-id="16484-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16484-111">-AsJob</span></span>
<span data-ttu-id="16484-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="16484-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16484-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16484-113">-DefaultProfile</span></span>
<span data-ttu-id="16484-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16484-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16484-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="16484-115">-ExtensionProperty</span></span>
<span data-ttu-id="16484-116">Właściwości rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="16484-116">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="16484-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="16484-117">-Location</span></span>
<span data-ttu-id="16484-118">Lokalizacja konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="16484-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="16484-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="16484-119">-MaintenanceScope</span></span>
<span data-ttu-id="16484-120">Zakres konserwacji.</span><span class="sxs-lookup"><span data-stu-id="16484-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="16484-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16484-121">-Name</span></span>
<span data-ttu-id="16484-122">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="16484-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="16484-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16484-123">-ResourceGroupName</span></span>
<span data-ttu-id="16484-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16484-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="16484-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="16484-125">-Tag</span></span>
<span data-ttu-id="16484-126">Znaczniki ARM.</span><span class="sxs-lookup"><span data-stu-id="16484-126">The ARM Tags.</span></span>

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

### <span data-ttu-id="16484-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16484-127">-Confirm</span></span>
<span data-ttu-id="16484-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16484-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16484-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16484-129">-WhatIf</span></span>
<span data-ttu-id="16484-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16484-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16484-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16484-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16484-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16484-132">CommonParameters</span></span>
<span data-ttu-id="16484-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16484-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16484-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16484-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16484-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16484-135">INPUTS</span></span>

### <span data-ttu-id="16484-136">System. String</span><span class="sxs-lookup"><span data-stu-id="16484-136">System.String</span></span>

## <span data-ttu-id="16484-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16484-137">OUTPUTS</span></span>

### <span data-ttu-id="16484-138">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="16484-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="16484-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16484-139">NOTES</span></span>

## <span data-ttu-id="16484-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16484-140">RELATED LINKS</span></span>

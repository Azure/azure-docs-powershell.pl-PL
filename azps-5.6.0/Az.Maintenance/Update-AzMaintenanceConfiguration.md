---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985937"
---
# <span data-ttu-id="b15c0-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15c0-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b15c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b15c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b15c0-103">Rekord konfiguracji poprawki</span><span class="sxs-lookup"><span data-stu-id="b15c0-103">Patch configuration record</span></span>

## <span data-ttu-id="b15c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b15c0-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b15c0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b15c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b15c0-106">Rekord konfiguracji konserwacji poprawek</span><span class="sxs-lookup"><span data-stu-id="b15c0-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="b15c0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b15c0-107">EXAMPLES</span></span>

### <span data-ttu-id="b15c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b15c0-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="b15c0-109">Rekord konfiguracji konserwacji poprawek</span><span class="sxs-lookup"><span data-stu-id="b15c0-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="b15c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b15c0-110">PARAMETERS</span></span>

### <span data-ttu-id="b15c0-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b15c0-111">-AsJob</span></span>
<span data-ttu-id="b15c0-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b15c0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b15c0-113">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="b15c0-113">-Configuration</span></span>
<span data-ttu-id="b15c0-114">Konfiguracja konserwacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b15c0-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b15c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15c0-115">-DefaultProfile</span></span>
<span data-ttu-id="b15c0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b15c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15c0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b15c0-117">-Name</span></span>
<span data-ttu-id="b15c0-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="b15c0-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="b15c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="b15c0-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b15c0-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="b15c0-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b15c0-121">-Confirm</span></span>
<span data-ttu-id="b15c0-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b15c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15c0-123">-WhatIf</span></span>
<span data-ttu-id="b15c0-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b15c0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b15c0-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b15c0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15c0-126">CommonParameters</span></span>
<span data-ttu-id="b15c0-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b15c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15c0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b15c0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15c0-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b15c0-129">INPUTS</span></span>

### <span data-ttu-id="b15c0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b15c0-130">System.String</span></span>

### <span data-ttu-id="b15c0-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15c0-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="b15c0-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b15c0-132">OUTPUTS</span></span>

### <span data-ttu-id="b15c0-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15c0-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="b15c0-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b15c0-134">NOTES</span></span>

## <span data-ttu-id="b15c0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b15c0-135">RELATED LINKS</span></span>

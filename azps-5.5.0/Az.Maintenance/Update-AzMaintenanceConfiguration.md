---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192266"
---
# <span data-ttu-id="89a83-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a83-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="89a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a83-102">SYNOPSIS</span></span>
<span data-ttu-id="89a83-103">Rekord konfiguracji poprawek</span><span class="sxs-lookup"><span data-stu-id="89a83-103">Patch configuration record</span></span>

## <span data-ttu-id="89a83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="89a83-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="89a83-105">DESCRIPTION</span></span>
<span data-ttu-id="89a83-106">Rekord konfiguracji konserwacji poprawek</span><span class="sxs-lookup"><span data-stu-id="89a83-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="89a83-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="89a83-107">EXAMPLES</span></span>

### <span data-ttu-id="89a83-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89a83-108">Example 1</span></span>
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

<span data-ttu-id="89a83-109">Rekord konfiguracji konserwacji poprawek</span><span class="sxs-lookup"><span data-stu-id="89a83-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="89a83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89a83-110">PARAMETERS</span></span>

### <span data-ttu-id="89a83-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="89a83-111">-AsJob</span></span>
<span data-ttu-id="89a83-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="89a83-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89a83-113">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="89a83-113">-Configuration</span></span>
<span data-ttu-id="89a83-114">Konfiguracja konserwacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="89a83-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="89a83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a83-115">-DefaultProfile</span></span>
<span data-ttu-id="89a83-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="89a83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89a83-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="89a83-117">-Name</span></span>
<span data-ttu-id="89a83-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="89a83-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="89a83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a83-119">-ResourceGroupName</span></span>
<span data-ttu-id="89a83-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="89a83-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="89a83-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89a83-121">-Confirm</span></span>
<span data-ttu-id="89a83-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="89a83-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a83-123">-WhatIf</span></span>
<span data-ttu-id="89a83-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a83-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="89a83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a83-126">CommonParameters</span></span>
<span data-ttu-id="89a83-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a83-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89a83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a83-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89a83-129">INPUTS</span></span>

### <span data-ttu-id="89a83-130">System.String</span><span class="sxs-lookup"><span data-stu-id="89a83-130">System.String</span></span>

### <span data-ttu-id="89a83-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a83-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="89a83-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89a83-132">OUTPUTS</span></span>

### <span data-ttu-id="89a83-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a83-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="89a83-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="89a83-134">NOTES</span></span>

## <span data-ttu-id="89a83-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89a83-135">RELATED LINKS</span></span>

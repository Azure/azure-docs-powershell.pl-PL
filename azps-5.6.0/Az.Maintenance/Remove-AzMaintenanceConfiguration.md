---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 2cebdeab994926d51ff5ff49e6a4a101f3e5c778
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985944"
---
# <span data-ttu-id="4bb0f-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bb0f-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="4bb0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb0f-103">Usuwanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="4bb0f-103">Delete Configuration record</span></span>

## <span data-ttu-id="4bb0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4bb0f-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb0f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4bb0f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb0f-106">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="4bb0f-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="4bb0f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4bb0f-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb0f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bb0f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="4bb0f-109">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="4bb0f-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="4bb0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb0f-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb0f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4bb0f-111">-AsJob</span></span>
<span data-ttu-id="4bb0f-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4bb0f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bb0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb0f-113">-DefaultProfile</span></span>
<span data-ttu-id="4bb0f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb0f-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4bb0f-115">-Force</span></span>
<span data-ttu-id="4bb0f-116">Wymusz usunięcie bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="4bb0f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4bb0f-117">-Name</span></span>
<span data-ttu-id="4bb0f-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="4bb0f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bb0f-119">-PassThru</span></span>
<span data-ttu-id="4bb0f-120">Zwraca stan operacji Usuń.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="4bb0f-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4bb0f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb0f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bb0f-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="4bb0f-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bb0f-124">-Confirm</span></span>
<span data-ttu-id="4bb0f-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb0f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb0f-126">-WhatIf</span></span>
<span data-ttu-id="4bb0f-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb0f-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb0f-129">CommonParameters</span></span>
<span data-ttu-id="4bb0f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb0f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bb0f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb0f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb0f-132">INPUTS</span></span>

### <span data-ttu-id="4bb0f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb0f-133">System.String</span></span>

## <span data-ttu-id="4bb0f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb0f-134">OUTPUTS</span></span>

### <span data-ttu-id="4bb0f-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bb0f-135">System.Boolean</span></span>

## <span data-ttu-id="4bb0f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4bb0f-136">NOTES</span></span>

## <span data-ttu-id="4bb0f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bb0f-137">RELATED LINKS</span></span>

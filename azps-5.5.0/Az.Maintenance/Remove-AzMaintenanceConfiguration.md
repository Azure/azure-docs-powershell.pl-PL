---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185138"
---
# <span data-ttu-id="03bac-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bac-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="03bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bac-102">SYNOPSIS</span></span>
<span data-ttu-id="03bac-103">Usuwanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="03bac-103">Delete Configuration record</span></span>

## <span data-ttu-id="03bac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03bac-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="03bac-105">DESCRIPTION</span></span>
<span data-ttu-id="03bac-106">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="03bac-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="03bac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03bac-107">EXAMPLES</span></span>

### <span data-ttu-id="03bac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03bac-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="03bac-109">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="03bac-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="03bac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03bac-110">PARAMETERS</span></span>

### <span data-ttu-id="03bac-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="03bac-111">-AsJob</span></span>
<span data-ttu-id="03bac-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03bac-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03bac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bac-113">-DefaultProfile</span></span>
<span data-ttu-id="03bac-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03bac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bac-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="03bac-115">-Force</span></span>
<span data-ttu-id="03bac-116">Wymusz usunięcie bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="03bac-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="03bac-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03bac-117">-Name</span></span>
<span data-ttu-id="03bac-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="03bac-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="03bac-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03bac-119">-PassThru</span></span>
<span data-ttu-id="03bac-120">Zwraca stan operacji Usuń.</span><span class="sxs-lookup"><span data-stu-id="03bac-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="03bac-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="03bac-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03bac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bac-122">-ResourceGroupName</span></span>
<span data-ttu-id="03bac-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03bac-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="03bac-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03bac-124">-Confirm</span></span>
<span data-ttu-id="03bac-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03bac-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bac-126">-WhatIf</span></span>
<span data-ttu-id="03bac-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03bac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bac-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03bac-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bac-129">CommonParameters</span></span>
<span data-ttu-id="03bac-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bac-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03bac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bac-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03bac-132">INPUTS</span></span>

### <span data-ttu-id="03bac-133">System.String</span><span class="sxs-lookup"><span data-stu-id="03bac-133">System.String</span></span>

## <span data-ttu-id="03bac-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03bac-134">OUTPUTS</span></span>

### <span data-ttu-id="03bac-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03bac-135">System.Boolean</span></span>

## <span data-ttu-id="03bac-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03bac-136">NOTES</span></span>

## <span data-ttu-id="03bac-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03bac-137">RELATED LINKS</span></span>

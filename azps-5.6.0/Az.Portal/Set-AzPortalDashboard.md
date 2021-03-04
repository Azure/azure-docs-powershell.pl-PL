---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988954"
---
# <span data-ttu-id="232b0-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="232b0-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="232b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="232b0-102">SYNOPSIS</span></span>
<span data-ttu-id="232b0-103">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="232b0-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="232b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="232b0-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="232b0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="232b0-105">DESCRIPTION</span></span>
<span data-ttu-id="232b0-106">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="232b0-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="232b0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="232b0-107">EXAMPLES</span></span>

### <span data-ttu-id="232b0-108">Przykład 1. Aktualizowanie definicji pulpitu nawigacyjnego przy użyciu szablonu pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="232b0-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="232b0-109">Zaktualizuj definicję pulpitu nawigacyjnego przy użyciu pliku szablonu kreskabaordu.</span><span class="sxs-lookup"><span data-stu-id="232b0-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="232b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="232b0-110">PARAMETERS</span></span>

### <span data-ttu-id="232b0-111">- DashboardPath</span><span class="sxs-lookup"><span data-stu-id="232b0-111">-DashboardPath</span></span>
<span data-ttu-id="232b0-112">Ścieżka do istniejącego szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="232b0-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="232b0-113">Szablony pulpitów nawigacyjnych można pobierać z portalu.</span><span class="sxs-lookup"><span data-stu-id="232b0-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="232b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232b0-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232b0-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="232b0-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232b0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232b0-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="232b0-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="232b0-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232b0-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="232b0-118">-Confirm</span></span>
<span data-ttu-id="232b0-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="232b0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232b0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232b0-120">-WhatIf</span></span>
<span data-ttu-id="232b0-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232b0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232b0-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="232b0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232b0-123">CommonParameters</span></span>
<span data-ttu-id="232b0-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232b0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="232b0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232b0-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="232b0-126">INPUTS</span></span>

## <span data-ttu-id="232b0-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="232b0-127">OUTPUTS</span></span>

### <span data-ttu-id="232b0-128">Microsoft.Azure.PowerShell.Cmdlet.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="232b0-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="232b0-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="232b0-129">NOTES</span></span>

<span data-ttu-id="232b0-130">ALIASY</span><span class="sxs-lookup"><span data-stu-id="232b0-130">ALIASES</span></span>

## <span data-ttu-id="232b0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="232b0-131">RELATED LINKS</span></span>


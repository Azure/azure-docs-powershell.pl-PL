---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309061"
---
# <span data-ttu-id="d166b-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="d166b-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="d166b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d166b-102">SYNOPSIS</span></span>
<span data-ttu-id="d166b-103">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="d166b-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="d166b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d166b-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d166b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d166b-105">DESCRIPTION</span></span>
<span data-ttu-id="d166b-106">Tworzy lub aktualizuje pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="d166b-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="d166b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d166b-107">EXAMPLES</span></span>

### <span data-ttu-id="d166b-108">Przykład 1: aktualizowanie definicji pulpitu nawigacyjnego przy użyciu szablonu pulpitu nawigacyjnego</span><span class="sxs-lookup"><span data-stu-id="d166b-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="d166b-109">Aktualizowanie definicji pulpitu nawigacyjnego przy użyciu pliku szablonu dashbaord.</span><span class="sxs-lookup"><span data-stu-id="d166b-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="d166b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d166b-110">PARAMETERS</span></span>

### <span data-ttu-id="d166b-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="d166b-111">-DashboardPath</span></span>
<span data-ttu-id="d166b-112">Ścieżka do istniejącego szablonu pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="d166b-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="d166b-113">Szablony pulpitu nawigacyjnego mogą być pobierane z portalu.</span><span class="sxs-lookup"><span data-stu-id="d166b-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="d166b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d166b-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="d166b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d166b-115">-Name</span></span>


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

### <span data-ttu-id="d166b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d166b-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="d166b-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d166b-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="d166b-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d166b-118">-Confirm</span></span>
<span data-ttu-id="d166b-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d166b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d166b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d166b-120">-WhatIf</span></span>
<span data-ttu-id="d166b-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d166b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d166b-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d166b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d166b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d166b-123">CommonParameters</span></span>
<span data-ttu-id="d166b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d166b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d166b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d166b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d166b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d166b-126">INPUTS</span></span>

## <span data-ttu-id="d166b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d166b-127">OUTPUTS</span></span>

### <span data-ttu-id="d166b-128">Microsoft. Azure. PowerShell. cmdlet. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="d166b-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="d166b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d166b-129">NOTES</span></span>

<span data-ttu-id="d166b-130">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d166b-130">ALIASES</span></span>

## <span data-ttu-id="d166b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d166b-131">RELATED LINKS</span></span>


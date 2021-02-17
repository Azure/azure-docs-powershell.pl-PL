---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182867"
---
# <span data-ttu-id="9d9db-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="9d9db-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="9d9db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d9db-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9db-103">Tworzy nowy alias i subskrypcję</span><span class="sxs-lookup"><span data-stu-id="9d9db-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="9d9db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d9db-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9db-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d9db-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9db-106">Polecenie **cmdlet New-AzSubscriptionAlias** tworzy nowy alias i subskrypcję</span><span class="sxs-lookup"><span data-stu-id="9d9db-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="9d9db-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d9db-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9db-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d9db-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="9d9db-109">Tworzy nowy alias i subskrypcję</span><span class="sxs-lookup"><span data-stu-id="9d9db-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="9d9db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d9db-110">PARAMETERS</span></span>

### <span data-ttu-id="9d9db-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9d9db-111">-AliasName</span></span>
<span data-ttu-id="9d9db-112">Alias dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9d9db-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="9d9db-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9db-113">-AsJob</span></span>
<span data-ttu-id="9d9db-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9d9db-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9db-115">- BillingScope</span><span class="sxs-lookup"><span data-stu-id="9d9db-115">-BillingScope</span></span>
<span data-ttu-id="9d9db-116">Zakres rozliczeń</span><span class="sxs-lookup"><span data-stu-id="9d9db-116">Billing Scope</span></span>

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

### <span data-ttu-id="9d9db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9db-117">-DefaultProfile</span></span>
<span data-ttu-id="9d9db-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9db-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="9d9db-119">-ResellerId</span></span>
<span data-ttu-id="9d9db-120">Identyfikator odsprzedawcy</span><span class="sxs-lookup"><span data-stu-id="9d9db-120">Reseller Id</span></span>

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

### <span data-ttu-id="9d9db-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d9db-121">-SubscriptionId</span></span>
<span data-ttu-id="9d9db-122">Istniejący identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9d9db-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="9d9db-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9d9db-123">-SubscriptionName</span></span>
<span data-ttu-id="9d9db-124">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9d9db-124">Name of the subscription</span></span>

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

### <span data-ttu-id="9d9db-125">— Obciążenie pracą</span><span class="sxs-lookup"><span data-stu-id="9d9db-125">-Workload</span></span>
<span data-ttu-id="9d9db-126">Typ obciążenia pracą</span><span class="sxs-lookup"><span data-stu-id="9d9db-126">Type of Workload</span></span>

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

### <span data-ttu-id="9d9db-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d9db-127">-Confirm</span></span>
<span data-ttu-id="9d9db-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d9db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9db-129">-WhatIf</span></span>
<span data-ttu-id="9d9db-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9db-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d9db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9db-132">CommonParameters</span></span>
<span data-ttu-id="9d9db-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9db-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d9db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9db-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d9db-135">INPUTS</span></span>

### <span data-ttu-id="9d9db-136">Brak</span><span class="sxs-lookup"><span data-stu-id="9d9db-136">None</span></span>

## <span data-ttu-id="9d9db-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d9db-137">OUTPUTS</span></span>

### <span data-ttu-id="9d9db-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9d9db-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="9d9db-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d9db-139">NOTES</span></span>

## <span data-ttu-id="9d9db-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d9db-140">RELATED LINKS</span></span>

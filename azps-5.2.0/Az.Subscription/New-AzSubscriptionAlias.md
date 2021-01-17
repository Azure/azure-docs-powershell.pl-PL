---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367950"
---
# <span data-ttu-id="f2bd0-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="f2bd0-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="f2bd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bd0-103">Tworzy nowy alias i abonament.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="f2bd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2bd0-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2bd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bd0-106">Polecenie cmdlet **New-AzSubscriptionAlias** tworzy nowy alias i abonament</span><span class="sxs-lookup"><span data-stu-id="f2bd0-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="f2bd0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="f2bd0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2bd0-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="f2bd0-109">Tworzy nowy alias i abonament.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="f2bd0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="f2bd0-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="f2bd0-111">-AliasName</span></span>
<span data-ttu-id="f2bd0-112">Alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2bd0-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="f2bd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2bd0-113">-AsJob</span></span>
<span data-ttu-id="f2bd0-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f2bd0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2bd0-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="f2bd0-115">-BillingScope</span></span>
<span data-ttu-id="f2bd0-116">Zakres rozliczeń</span><span class="sxs-lookup"><span data-stu-id="f2bd0-116">Billing Scope</span></span>

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

### <span data-ttu-id="f2bd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bd0-117">-DefaultProfile</span></span>
<span data-ttu-id="f2bd0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bd0-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="f2bd0-119">-ResellerId</span></span>
<span data-ttu-id="f2bd0-120">Identyfikator odsprzedawcy</span><span class="sxs-lookup"><span data-stu-id="f2bd0-120">Reseller Id</span></span>

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

### <span data-ttu-id="f2bd0-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2bd0-121">-SubscriptionId</span></span>
<span data-ttu-id="f2bd0-122">Identyfikator istniejącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2bd0-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="f2bd0-123">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="f2bd0-123">-SubscriptionName</span></span>
<span data-ttu-id="f2bd0-124">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2bd0-124">Name of the subscription</span></span>

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

### <span data-ttu-id="f2bd0-125">— Obciążenie pracą</span><span class="sxs-lookup"><span data-stu-id="f2bd0-125">-Workload</span></span>
<span data-ttu-id="f2bd0-126">Typ obciążenia</span><span class="sxs-lookup"><span data-stu-id="f2bd0-126">Type of Workload</span></span>

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

### <span data-ttu-id="f2bd0-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2bd0-127">-Confirm</span></span>
<span data-ttu-id="f2bd0-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2bd0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2bd0-129">-WhatIf</span></span>
<span data-ttu-id="f2bd0-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2bd0-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2bd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bd0-132">CommonParameters</span></span>
<span data-ttu-id="f2bd0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bd0-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2bd0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bd0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2bd0-135">INPUTS</span></span>

### <span data-ttu-id="f2bd0-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2bd0-136">None</span></span>

## <span data-ttu-id="f2bd0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2bd0-137">OUTPUTS</span></span>

### <span data-ttu-id="f2bd0-138">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f2bd0-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="f2bd0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2bd0-139">NOTES</span></span>

## <span data-ttu-id="f2bd0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2bd0-140">RELATED LINKS</span></span>

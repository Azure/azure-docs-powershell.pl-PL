---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182866"
---
# <span data-ttu-id="da438-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="da438-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="da438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da438-102">SYNOPSIS</span></span>
<span data-ttu-id="da438-103">Usuwa alias subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da438-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="da438-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da438-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da438-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="da438-105">DESCRIPTION</span></span>
<span data-ttu-id="da438-106">Polecenie **cmdlet Remove-AzSubscriptionAlias** usuwa alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da438-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="da438-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da438-107">EXAMPLES</span></span>

### <span data-ttu-id="da438-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da438-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="da438-109">Usuwa alias subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da438-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="da438-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da438-110">PARAMETERS</span></span>

### <span data-ttu-id="da438-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="da438-111">-AliasName</span></span>
<span data-ttu-id="da438-112">Alias dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da438-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="da438-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="da438-113">-AsJob</span></span>
<span data-ttu-id="da438-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="da438-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da438-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da438-115">-DefaultProfile</span></span>
<span data-ttu-id="da438-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da438-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da438-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da438-117">-Confirm</span></span>
<span data-ttu-id="da438-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da438-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da438-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da438-119">-WhatIf</span></span>
<span data-ttu-id="da438-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da438-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da438-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="da438-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da438-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da438-122">CommonParameters</span></span>
<span data-ttu-id="da438-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da438-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da438-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da438-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da438-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da438-125">INPUTS</span></span>

### <span data-ttu-id="da438-126">Brak</span><span class="sxs-lookup"><span data-stu-id="da438-126">None</span></span>

## <span data-ttu-id="da438-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da438-127">OUTPUTS</span></span>

### <span data-ttu-id="da438-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="da438-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="da438-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da438-129">NOTES</span></span>

## <span data-ttu-id="da438-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da438-130">RELATED LINKS</span></span>

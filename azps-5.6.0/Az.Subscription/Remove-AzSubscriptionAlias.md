---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971649"
---
# <span data-ttu-id="d4205-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="d4205-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="d4205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4205-102">SYNOPSIS</span></span>
<span data-ttu-id="d4205-103">Usuwa alias subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d4205-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="d4205-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4205-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4205-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4205-105">DESCRIPTION</span></span>
<span data-ttu-id="d4205-106">Polecenie **cmdlet Remove-AzSubscriptionAlias** usuwa alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d4205-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="d4205-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4205-107">EXAMPLES</span></span>

### <span data-ttu-id="d4205-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4205-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="d4205-109">Usuwa alias subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d4205-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="d4205-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4205-110">PARAMETERS</span></span>

### <span data-ttu-id="d4205-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="d4205-111">-AliasName</span></span>
<span data-ttu-id="d4205-112">Alias dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d4205-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="d4205-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d4205-113">-AsJob</span></span>
<span data-ttu-id="d4205-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d4205-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4205-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4205-115">-DefaultProfile</span></span>
<span data-ttu-id="d4205-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4205-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4205-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4205-117">-Confirm</span></span>
<span data-ttu-id="d4205-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d4205-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4205-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4205-119">-WhatIf</span></span>
<span data-ttu-id="d4205-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4205-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4205-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d4205-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4205-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4205-122">CommonParameters</span></span>
<span data-ttu-id="d4205-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4205-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4205-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4205-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4205-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4205-125">INPUTS</span></span>

### <span data-ttu-id="d4205-126">Brak</span><span class="sxs-lookup"><span data-stu-id="d4205-126">None</span></span>

## <span data-ttu-id="d4205-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4205-127">OUTPUTS</span></span>

### <span data-ttu-id="d4205-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d4205-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="d4205-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4205-129">NOTES</span></span>

## <span data-ttu-id="d4205-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4205-130">RELATED LINKS</span></span>

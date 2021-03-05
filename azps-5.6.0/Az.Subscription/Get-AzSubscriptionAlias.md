---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988681"
---
# <span data-ttu-id="704b2-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="704b2-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="704b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="704b2-102">SYNOPSIS</span></span>
<span data-ttu-id="704b2-103">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="704b2-103">Gets subscription alias details</span></span>

## <span data-ttu-id="704b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="704b2-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704b2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="704b2-105">DESCRIPTION</span></span>
<span data-ttu-id="704b2-106">Polecenie **cmdlet Get-AzSubscriptionAlias** pobiera szczegóły aliasu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="704b2-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="704b2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="704b2-107">EXAMPLES</span></span>

### <span data-ttu-id="704b2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="704b2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="704b2-109">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="704b2-109">Gets subscription alias details</span></span>

## <span data-ttu-id="704b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="704b2-110">PARAMETERS</span></span>

### <span data-ttu-id="704b2-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="704b2-111">-AliasName</span></span>
<span data-ttu-id="704b2-112">Alias dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="704b2-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="704b2-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="704b2-113">-AsJob</span></span>
<span data-ttu-id="704b2-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="704b2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="704b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704b2-115">-DefaultProfile</span></span>
<span data-ttu-id="704b2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="704b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704b2-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="704b2-117">-Confirm</span></span>
<span data-ttu-id="704b2-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="704b2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704b2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704b2-119">-WhatIf</span></span>
<span data-ttu-id="704b2-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="704b2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704b2-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="704b2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704b2-122">CommonParameters</span></span>
<span data-ttu-id="704b2-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704b2-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="704b2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704b2-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="704b2-125">INPUTS</span></span>

### <span data-ttu-id="704b2-126">Brak</span><span class="sxs-lookup"><span data-stu-id="704b2-126">None</span></span>

## <span data-ttu-id="704b2-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="704b2-127">OUTPUTS</span></span>

### <span data-ttu-id="704b2-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="704b2-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="704b2-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="704b2-129">NOTES</span></span>

## <span data-ttu-id="704b2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="704b2-130">RELATED LINKS</span></span>

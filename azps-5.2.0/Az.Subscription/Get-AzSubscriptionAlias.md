---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370559"
---
# <span data-ttu-id="9c9b1-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="9c9b1-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="9c9b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9b1-103">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9c9b1-103">Gets subscription alias details</span></span>

## <span data-ttu-id="9c9b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c9b1-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c9b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c9b1-105">DESCRIPTION</span></span>
<span data-ttu-id="9c9b1-106">Polecenie cmdlet **Get-AzSubscriptionAlias** pobiera szczegóły aliasu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="9c9b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c9b1-107">EXAMPLES</span></span>

### <span data-ttu-id="9c9b1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c9b1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="9c9b1-109">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9c9b1-109">Gets subscription alias details</span></span>

## <span data-ttu-id="9c9b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c9b1-110">PARAMETERS</span></span>

### <span data-ttu-id="9c9b1-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="9c9b1-111">-AliasName</span></span>
<span data-ttu-id="9c9b1-112">Alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9c9b1-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="9c9b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c9b1-113">-AsJob</span></span>
<span data-ttu-id="9c9b1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c9b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c9b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9b1-115">-DefaultProfile</span></span>
<span data-ttu-id="9c9b1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9b1-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c9b1-117">-Confirm</span></span>
<span data-ttu-id="9c9b1-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9b1-119">-WhatIf</span></span>
<span data-ttu-id="9c9b1-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c9b1-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9b1-122">CommonParameters</span></span>
<span data-ttu-id="9c9b1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9b1-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c9b1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9b1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c9b1-125">INPUTS</span></span>

### <span data-ttu-id="9c9b1-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9c9b1-126">None</span></span>

## <span data-ttu-id="9c9b1-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c9b1-127">OUTPUTS</span></span>

### <span data-ttu-id="9c9b1-128">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c9b1-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="9c9b1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c9b1-129">NOTES</span></span>

## <span data-ttu-id="9c9b1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c9b1-130">RELATED LINKS</span></span>

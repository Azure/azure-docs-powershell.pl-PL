---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232448"
---
# <span data-ttu-id="01344-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="01344-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="01344-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01344-102">SYNOPSIS</span></span>
<span data-ttu-id="01344-103">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="01344-103">Gets subscription alias details</span></span>

## <span data-ttu-id="01344-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01344-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01344-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01344-105">DESCRIPTION</span></span>
<span data-ttu-id="01344-106">Polecenie cmdlet **Get-AzSubscriptionAlias** pobiera szczegóły aliasu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="01344-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="01344-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01344-107">EXAMPLES</span></span>

### <span data-ttu-id="01344-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01344-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="01344-109">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="01344-109">Gets subscription alias details</span></span>

## <span data-ttu-id="01344-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01344-110">PARAMETERS</span></span>

### <span data-ttu-id="01344-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="01344-111">-AliasName</span></span>
<span data-ttu-id="01344-112">Alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="01344-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="01344-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01344-113">-AsJob</span></span>
<span data-ttu-id="01344-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="01344-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01344-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01344-115">-DefaultProfile</span></span>
<span data-ttu-id="01344-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01344-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01344-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01344-117">-Confirm</span></span>
<span data-ttu-id="01344-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01344-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01344-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01344-119">-WhatIf</span></span>
<span data-ttu-id="01344-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01344-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01344-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01344-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01344-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01344-122">CommonParameters</span></span>
<span data-ttu-id="01344-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01344-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01344-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01344-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01344-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01344-125">INPUTS</span></span>

### <span data-ttu-id="01344-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="01344-126">None</span></span>

## <span data-ttu-id="01344-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01344-127">OUTPUTS</span></span>

### <span data-ttu-id="01344-128">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="01344-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="01344-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01344-129">NOTES</span></span>

## <span data-ttu-id="01344-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01344-130">RELATED LINKS</span></span>

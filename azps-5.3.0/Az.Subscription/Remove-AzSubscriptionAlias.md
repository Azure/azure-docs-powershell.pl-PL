---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491161"
---
# <span data-ttu-id="d90d0-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="d90d0-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="d90d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d90d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d90d0-103">Usuwa alias abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d90d0-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="d90d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d90d0-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d90d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d90d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d90d0-106">Polecenie cmdlet **Remove-AzSubscriptionAlias** usuwa alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d90d0-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="d90d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d90d0-107">EXAMPLES</span></span>

### <span data-ttu-id="d90d0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d90d0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="d90d0-109">Usuwa alias abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d90d0-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="d90d0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d90d0-110">PARAMETERS</span></span>

### <span data-ttu-id="d90d0-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="d90d0-111">-AliasName</span></span>
<span data-ttu-id="d90d0-112">Alias subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d90d0-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="d90d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d90d0-113">-AsJob</span></span>
<span data-ttu-id="d90d0-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d90d0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d90d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90d0-115">-DefaultProfile</span></span>
<span data-ttu-id="d90d0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d90d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d90d0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d90d0-117">-Confirm</span></span>
<span data-ttu-id="d90d0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d90d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90d0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90d0-119">-WhatIf</span></span>
<span data-ttu-id="d90d0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d90d0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90d0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d90d0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90d0-122">CommonParameters</span></span>
<span data-ttu-id="d90d0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90d0-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d90d0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90d0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d90d0-125">INPUTS</span></span>

### <span data-ttu-id="d90d0-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d90d0-126">None</span></span>

## <span data-ttu-id="d90d0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d90d0-127">OUTPUTS</span></span>

### <span data-ttu-id="d90d0-128">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d90d0-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="d90d0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d90d0-129">NOTES</span></span>

## <span data-ttu-id="d90d0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d90d0-130">RELATED LINKS</span></span>

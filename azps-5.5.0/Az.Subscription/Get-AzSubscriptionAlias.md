---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182882"
---
# <span data-ttu-id="03598-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="03598-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="03598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03598-102">SYNOPSIS</span></span>
<span data-ttu-id="03598-103">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03598-103">Gets subscription alias details</span></span>

## <span data-ttu-id="03598-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03598-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03598-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="03598-105">DESCRIPTION</span></span>
<span data-ttu-id="03598-106">Polecenie **cmdlet Get-AzSubscriptionAlias** pobiera szczegóły aliasu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="03598-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="03598-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03598-107">EXAMPLES</span></span>

### <span data-ttu-id="03598-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03598-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="03598-109">Pobiera szczegóły aliasu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03598-109">Gets subscription alias details</span></span>

## <span data-ttu-id="03598-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03598-110">PARAMETERS</span></span>

### <span data-ttu-id="03598-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="03598-111">-AliasName</span></span>
<span data-ttu-id="03598-112">Alias dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03598-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="03598-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="03598-113">-AsJob</span></span>
<span data-ttu-id="03598-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03598-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03598-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03598-115">-DefaultProfile</span></span>
<span data-ttu-id="03598-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03598-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03598-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03598-117">-Confirm</span></span>
<span data-ttu-id="03598-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03598-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03598-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03598-119">-WhatIf</span></span>
<span data-ttu-id="03598-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03598-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03598-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03598-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03598-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03598-122">CommonParameters</span></span>
<span data-ttu-id="03598-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03598-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03598-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03598-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03598-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03598-125">INPUTS</span></span>

### <span data-ttu-id="03598-126">Brak</span><span class="sxs-lookup"><span data-stu-id="03598-126">None</span></span>

## <span data-ttu-id="03598-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03598-127">OUTPUTS</span></span>

### <span data-ttu-id="03598-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="03598-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="03598-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03598-129">NOTES</span></span>

## <span data-ttu-id="03598-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03598-130">RELATED LINKS</span></span>

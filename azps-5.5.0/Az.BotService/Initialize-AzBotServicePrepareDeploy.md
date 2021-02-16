---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200851"
---
# <span data-ttu-id="e05c0-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="e05c0-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="e05c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e05c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e05c0-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="e05c0-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="e05c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e05c0-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e05c0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e05c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e05c0-106">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="e05c0-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="e05c0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e05c0-107">EXAMPLES</span></span>

### <span data-ttu-id="e05c0-108">Przykład 1. Inicjowanie pliku projektu</span><span class="sxs-lookup"><span data-stu-id="e05c0-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="e05c0-109">Zainicjowanie przygotowywanie zasobu do użycia i ustawienie go jako stanu domyślnego</span><span class="sxs-lookup"><span data-stu-id="e05c0-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="e05c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e05c0-110">PARAMETERS</span></span>

### <span data-ttu-id="e05c0-111">- CodeDir</span><span class="sxs-lookup"><span data-stu-id="e05c0-111">-CodeDir</span></span>
<span data-ttu-id="e05c0-112">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e05c0-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="e05c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05c0-113">-DefaultProfile</span></span>
<span data-ttu-id="e05c0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e05c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05c0-115">— język</span><span class="sxs-lookup"><span data-stu-id="e05c0-115">-Language</span></span>


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

### <span data-ttu-id="e05c0-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="e05c0-116">-ProjFileName</span></span>


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

### <span data-ttu-id="e05c0-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e05c0-117">-SubscriptionId</span></span>
<span data-ttu-id="e05c0-118">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e05c0-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05c0-119">CommonParameters</span></span>
<span data-ttu-id="e05c0-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05c0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e05c0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05c0-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e05c0-122">INPUTS</span></span>

## <span data-ttu-id="e05c0-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e05c0-123">OUTPUTS</span></span>

### <span data-ttu-id="e05c0-124">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="e05c0-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="e05c0-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e05c0-125">NOTES</span></span>

<span data-ttu-id="e05c0-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e05c0-126">ALIASES</span></span>

## <span data-ttu-id="e05c0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e05c0-127">RELATED LINKS</span></span>


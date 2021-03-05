---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009306"
---
# <span data-ttu-id="de5da-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="de5da-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="de5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de5da-102">SYNOPSIS</span></span>
<span data-ttu-id="de5da-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="de5da-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="de5da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de5da-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="de5da-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de5da-105">DESCRIPTION</span></span>
<span data-ttu-id="de5da-106">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="de5da-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="de5da-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de5da-107">EXAMPLES</span></span>

### <span data-ttu-id="de5da-108">Przykład 1. Inicjowanie pliku projektu</span><span class="sxs-lookup"><span data-stu-id="de5da-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="de5da-109">Zainicjowanie przygotowywanie zasobu do użycia i ustawienie go jako stanu domyślnego</span><span class="sxs-lookup"><span data-stu-id="de5da-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="de5da-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de5da-110">PARAMETERS</span></span>

### <span data-ttu-id="de5da-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="de5da-111">-CodeDir</span></span>
<span data-ttu-id="de5da-112">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="de5da-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="de5da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5da-113">-DefaultProfile</span></span>
<span data-ttu-id="de5da-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de5da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5da-115">— język</span><span class="sxs-lookup"><span data-stu-id="de5da-115">-Language</span></span>


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

### <span data-ttu-id="de5da-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="de5da-116">-ProjFileName</span></span>


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

### <span data-ttu-id="de5da-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de5da-117">-SubscriptionId</span></span>
<span data-ttu-id="de5da-118">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de5da-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="de5da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5da-119">CommonParameters</span></span>
<span data-ttu-id="de5da-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5da-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de5da-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5da-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de5da-122">INPUTS</span></span>

## <span data-ttu-id="de5da-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de5da-123">OUTPUTS</span></span>

### <span data-ttu-id="de5da-124">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="de5da-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="de5da-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de5da-125">NOTES</span></span>

<span data-ttu-id="de5da-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="de5da-126">ALIASES</span></span>

## <span data-ttu-id="de5da-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de5da-127">RELATED LINKS</span></span>


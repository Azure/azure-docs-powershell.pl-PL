---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504227"
---
# <span data-ttu-id="2de4a-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="2de4a-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="2de4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2de4a-102">SYNOPSIS</span></span>
<span data-ttu-id="2de4a-103">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="2de4a-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2de4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2de4a-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2de4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2de4a-105">DESCRIPTION</span></span>
<span data-ttu-id="2de4a-106">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="2de4a-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2de4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2de4a-107">EXAMPLES</span></span>

### <span data-ttu-id="2de4a-108">Przykład 1. inicjowanie projektu FileFolder</span><span class="sxs-lookup"><span data-stu-id="2de4a-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="2de4a-109">Initialize przygotowuje zasób do użycia i ustawia go na stan domyślny</span><span class="sxs-lookup"><span data-stu-id="2de4a-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="2de4a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2de4a-110">PARAMETERS</span></span>

### <span data-ttu-id="2de4a-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="2de4a-111">-CodeDir</span></span>
<span data-ttu-id="2de4a-112">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2de4a-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="2de4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de4a-113">-DefaultProfile</span></span>
<span data-ttu-id="2de4a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2de4a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de4a-115">-Language</span><span class="sxs-lookup"><span data-stu-id="2de4a-115">-Language</span></span>


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

### <span data-ttu-id="2de4a-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="2de4a-116">-ProjFileName</span></span>


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

### <span data-ttu-id="2de4a-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2de4a-117">-SubscriptionId</span></span>
<span data-ttu-id="2de4a-118">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2de4a-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2de4a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de4a-119">CommonParameters</span></span>
<span data-ttu-id="2de4a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de4a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de4a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2de4a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de4a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2de4a-122">INPUTS</span></span>

## <span data-ttu-id="2de4a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2de4a-123">OUTPUTS</span></span>

### <span data-ttu-id="2de4a-124">Microsoft. Azure. PowerShell. polecenia. BotService. models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="2de4a-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="2de4a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2de4a-125">NOTES</span></span>

<span data-ttu-id="2de4a-126">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2de4a-126">ALIASES</span></span>

## <span data-ttu-id="2de4a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2de4a-127">RELATED LINKS</span></span>


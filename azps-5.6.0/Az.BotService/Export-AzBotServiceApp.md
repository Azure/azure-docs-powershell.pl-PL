---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960874"
---
# <span data-ttu-id="d9459-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="d9459-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="d9459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9459-102">SYNOPSIS</span></span>
<span data-ttu-id="d9459-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="d9459-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d9459-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9459-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9459-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9459-105">DESCRIPTION</span></span>
<span data-ttu-id="d9459-106">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="d9459-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d9459-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9459-107">EXAMPLES</span></span>

### <span data-ttu-id="d9459-108">Przykład 1. Ładowanie w dół folderu aplikacji BotService</span><span class="sxs-lookup"><span data-stu-id="d9459-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="d9459-109">Załaduj w dół folder aplikacji BotService</span><span class="sxs-lookup"><span data-stu-id="d9459-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="d9459-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9459-110">PARAMETERS</span></span>

### <span data-ttu-id="d9459-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9459-111">-DefaultProfile</span></span>
<span data-ttu-id="d9459-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9459-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9459-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9459-113">-Name</span></span>
<span data-ttu-id="d9459-114">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="d9459-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9459-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9459-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9459-116">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9459-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="d9459-117">— SavePath</span><span class="sxs-lookup"><span data-stu-id="d9459-117">-SavePath</span></span>


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

### <span data-ttu-id="d9459-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9459-118">-SubscriptionId</span></span>
<span data-ttu-id="d9459-119">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9459-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d9459-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9459-120">CommonParameters</span></span>
<span data-ttu-id="d9459-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9459-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9459-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9459-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9459-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9459-123">INPUTS</span></span>

## <span data-ttu-id="d9459-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9459-124">OUTPUTS</span></span>

### <span data-ttu-id="d9459-125">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="d9459-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d9459-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9459-126">NOTES</span></span>

<span data-ttu-id="d9459-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d9459-127">ALIASES</span></span>

## <span data-ttu-id="d9459-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9459-128">RELATED LINKS</span></span>


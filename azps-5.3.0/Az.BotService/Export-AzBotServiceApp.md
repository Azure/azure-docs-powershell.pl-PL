---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504228"
---
# <span data-ttu-id="3cf8b-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="3cf8b-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="3cf8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cf8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf8b-103">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3cf8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cf8b-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3cf8b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cf8b-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf8b-106">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3cf8b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cf8b-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf8b-108">Przykład 1. Pobierz folder aplikacji BotService</span><span class="sxs-lookup"><span data-stu-id="3cf8b-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="3cf8b-109">Pobierz folder aplikacji BotService</span><span class="sxs-lookup"><span data-stu-id="3cf8b-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="3cf8b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cf8b-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf8b-111">-DefaultProfile</span></span>
<span data-ttu-id="3cf8b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf8b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cf8b-113">-Name</span></span>
<span data-ttu-id="3cf8b-114">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="3cf8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="3cf8b-116">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="3cf8b-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="3cf8b-117">-SavePath</span></span>


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

### <span data-ttu-id="3cf8b-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3cf8b-118">-SubscriptionId</span></span>
<span data-ttu-id="3cf8b-119">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3cf8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf8b-120">CommonParameters</span></span>
<span data-ttu-id="3cf8b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf8b-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cf8b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf8b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cf8b-123">INPUTS</span></span>

## <span data-ttu-id="3cf8b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cf8b-124">OUTPUTS</span></span>

### <span data-ttu-id="3cf8b-125">Microsoft. Azure. PowerShell. polecenia. BotService. models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="3cf8b-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="3cf8b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cf8b-126">NOTES</span></span>

<span data-ttu-id="3cf8b-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3cf8b-127">ALIASES</span></span>

## <span data-ttu-id="3cf8b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cf8b-128">RELATED LINKS</span></span>


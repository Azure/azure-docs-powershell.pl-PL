---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980561"
---
# <span data-ttu-id="5fe14-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="5fe14-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="5fe14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe14-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe14-103">Elementy menu Start listy w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fe14-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="5fe14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5fe14-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5fe14-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5fe14-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe14-106">Elementy menu Start listy w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fe14-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="5fe14-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5fe14-107">EXAMPLES</span></span>

### <span data-ttu-id="5fe14-108">Przykład 2. Lista elementów menu Start pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="5fe14-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="5fe14-109">To polecenie wyświetla listę elementów menu Start pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fe14-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="5fe14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe14-110">PARAMETERS</span></span>

### <span data-ttu-id="5fe14-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe14-111">-ApplicationGroupName</span></span>
<span data-ttu-id="5fe14-112">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5fe14-112">The name of the application group</span></span>

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

### <span data-ttu-id="5fe14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe14-113">-DefaultProfile</span></span>
<span data-ttu-id="5fe14-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe14-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe14-115">-ResourceGroupName</span></span>
<span data-ttu-id="5fe14-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fe14-116">The name of the resource group.</span></span>
<span data-ttu-id="5fe14-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5fe14-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5fe14-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fe14-118">-SubscriptionId</span></span>
<span data-ttu-id="5fe14-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5fe14-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5fe14-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe14-120">CommonParameters</span></span>
<span data-ttu-id="5fe14-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe14-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe14-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fe14-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe14-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fe14-123">INPUTS</span></span>

## <span data-ttu-id="5fe14-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fe14-124">OUTPUTS</span></span>

### <span data-ttu-id="5fe14-125">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="5fe14-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="5fe14-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5fe14-126">NOTES</span></span>

<span data-ttu-id="5fe14-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5fe14-127">ALIASES</span></span>

## <span data-ttu-id="5fe14-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fe14-128">RELATED LINKS</span></span>


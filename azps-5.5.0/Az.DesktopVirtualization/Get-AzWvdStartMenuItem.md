---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: fd91ea79cbad51d03c0986ed5f55601af240de16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196451"
---
# <span data-ttu-id="b7755-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="b7755-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="b7755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7755-102">SYNOPSIS</span></span>
<span data-ttu-id="b7755-103">Elementy menu Start listy w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7755-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="b7755-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7755-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b7755-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7755-105">DESCRIPTION</span></span>
<span data-ttu-id="b7755-106">Elementy menu Start listy w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7755-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="b7755-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7755-107">EXAMPLES</span></span>

### <span data-ttu-id="b7755-108">Przykład 2. Lista elementów menu Start pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="b7755-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="b7755-109">To polecenie wyświetla listę elementów menu Start pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b7755-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="b7755-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7755-110">PARAMETERS</span></span>

### <span data-ttu-id="b7755-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b7755-111">-ApplicationGroupName</span></span>
<span data-ttu-id="b7755-112">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7755-112">The name of the application group</span></span>

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

### <span data-ttu-id="b7755-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7755-113">-DefaultProfile</span></span>
<span data-ttu-id="b7755-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7755-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7755-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7755-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7755-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7755-116">The name of the resource group.</span></span>
<span data-ttu-id="b7755-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b7755-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b7755-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7755-118">-SubscriptionId</span></span>
<span data-ttu-id="b7755-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b7755-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b7755-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7755-120">CommonParameters</span></span>
<span data-ttu-id="b7755-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7755-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7755-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7755-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7755-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7755-123">INPUTS</span></span>

## <span data-ttu-id="b7755-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7755-124">OUTPUTS</span></span>

### <span data-ttu-id="b7755-125">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="b7755-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="b7755-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7755-126">NOTES</span></span>

<span data-ttu-id="b7755-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b7755-127">ALIASES</span></span>

## <span data-ttu-id="b7755-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7755-128">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: 4ad2b7db5e212cf15748ac81ae28b9471d1678b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354205"
---
# <span data-ttu-id="81252-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="81252-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="81252-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81252-102">SYNOPSIS</span></span>
<span data-ttu-id="81252-103">Wyświetlanie listy elementów menu Start w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81252-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="81252-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81252-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81252-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81252-105">DESCRIPTION</span></span>
<span data-ttu-id="81252-106">Wyświetlanie listy elementów menu Start w danej grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81252-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="81252-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81252-107">EXAMPLES</span></span>

### <span data-ttu-id="81252-108">Przykład 2: Wyświetlanie elementów menu Start na pulpicie wirtualnym systemu Windows</span><span class="sxs-lookup"><span data-stu-id="81252-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="81252-109">To polecenie zawiera listę elementów menu Start pulpitu wirtualnego systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="81252-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="81252-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81252-110">PARAMETERS</span></span>

### <span data-ttu-id="81252-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="81252-111">-ApplicationGroupName</span></span>
<span data-ttu-id="81252-112">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="81252-112">The name of the application group</span></span>

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

### <span data-ttu-id="81252-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81252-113">-DefaultProfile</span></span>
<span data-ttu-id="81252-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81252-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81252-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81252-115">-ResourceGroupName</span></span>
<span data-ttu-id="81252-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81252-116">The name of the resource group.</span></span>
<span data-ttu-id="81252-117">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="81252-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="81252-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="81252-118">-SubscriptionId</span></span>
<span data-ttu-id="81252-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="81252-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="81252-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81252-120">CommonParameters</span></span>
<span data-ttu-id="81252-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81252-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81252-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81252-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81252-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81252-123">INPUTS</span></span>

## <span data-ttu-id="81252-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81252-124">OUTPUTS</span></span>

### <span data-ttu-id="81252-125">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="81252-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IStartMenuItem</span></span>

## <span data-ttu-id="81252-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81252-126">NOTES</span></span>

<span data-ttu-id="81252-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="81252-127">ALIASES</span></span>

## <span data-ttu-id="81252-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81252-128">RELATED LINKS</span></span>


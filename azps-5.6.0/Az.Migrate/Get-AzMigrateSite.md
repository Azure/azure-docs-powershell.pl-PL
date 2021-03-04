---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: b00010096b39cd714f01f33012309f8528a5ae3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982801"
---
# <span data-ttu-id="25b89-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="25b89-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="25b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b89-102">SYNOPSIS</span></span>
<span data-ttu-id="25b89-103">Metoda uzyskania witryny.</span><span class="sxs-lookup"><span data-stu-id="25b89-103">Method to get a site.</span></span>

## <span data-ttu-id="25b89-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25b89-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="25b89-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="25b89-105">DESCRIPTION</span></span>
<span data-ttu-id="25b89-106">Metoda uzyskania witryny.</span><span class="sxs-lookup"><span data-stu-id="25b89-106">Method to get a site.</span></span>

## <span data-ttu-id="25b89-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25b89-107">EXAMPLES</span></span>

### <span data-ttu-id="25b89-108">Przykład 1. Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="25b89-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="25b89-109">Uzyskiwanie witryny według nazwy</span><span class="sxs-lookup"><span data-stu-id="25b89-109">Get site by name</span></span>

## <span data-ttu-id="25b89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b89-110">PARAMETERS</span></span>

### <span data-ttu-id="25b89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b89-111">-DefaultProfile</span></span>
<span data-ttu-id="25b89-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25b89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b89-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25b89-113">-Name</span></span>
<span data-ttu-id="25b89-114">Nazwa witryny.</span><span class="sxs-lookup"><span data-stu-id="25b89-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b89-115">-ResourceGroupName</span></span>
<span data-ttu-id="25b89-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25b89-116">The name of the resource group.</span></span>
<span data-ttu-id="25b89-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="25b89-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="25b89-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25b89-118">-SubscriptionId</span></span>
<span data-ttu-id="25b89-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="25b89-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="25b89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b89-120">CommonParameters</span></span>
<span data-ttu-id="25b89-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b89-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25b89-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b89-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25b89-123">INPUTS</span></span>

## <span data-ttu-id="25b89-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25b89-124">OUTPUTS</span></span>

### <span data-ttu-id="25b89-125">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api202001.IVShellSite</span><span class="sxs-lookup"><span data-stu-id="25b89-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="25b89-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25b89-126">NOTES</span></span>

<span data-ttu-id="25b89-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="25b89-127">ALIASES</span></span>

## <span data-ttu-id="25b89-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25b89-128">RELATED LINKS</span></span>


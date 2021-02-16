---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180210"
---
# <span data-ttu-id="5eddd-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="5eddd-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="5eddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eddd-102">SYNOPSIS</span></span>
<span data-ttu-id="5eddd-103">Metoda uzyskania witryny.</span><span class="sxs-lookup"><span data-stu-id="5eddd-103">Method to get a site.</span></span>

## <span data-ttu-id="5eddd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5eddd-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5eddd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5eddd-105">DESCRIPTION</span></span>
<span data-ttu-id="5eddd-106">Metoda uzyskania witryny.</span><span class="sxs-lookup"><span data-stu-id="5eddd-106">Method to get a site.</span></span>

## <span data-ttu-id="5eddd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5eddd-107">EXAMPLES</span></span>

### <span data-ttu-id="5eddd-108">Przykład 1. Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5eddd-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="5eddd-109">Uzyskiwanie witryny według nazwy</span><span class="sxs-lookup"><span data-stu-id="5eddd-109">Get site by name</span></span>

## <span data-ttu-id="5eddd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eddd-110">PARAMETERS</span></span>

### <span data-ttu-id="5eddd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eddd-111">-DefaultProfile</span></span>
<span data-ttu-id="5eddd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5eddd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eddd-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5eddd-113">-Name</span></span>
<span data-ttu-id="5eddd-114">Nazwa witryny.</span><span class="sxs-lookup"><span data-stu-id="5eddd-114">Site name.</span></span>

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

### <span data-ttu-id="5eddd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eddd-115">-ResourceGroupName</span></span>
<span data-ttu-id="5eddd-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5eddd-116">The name of the resource group.</span></span>
<span data-ttu-id="5eddd-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="5eddd-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5eddd-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eddd-118">-SubscriptionId</span></span>
<span data-ttu-id="5eddd-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5eddd-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5eddd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eddd-120">CommonParameters</span></span>
<span data-ttu-id="5eddd-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eddd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eddd-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eddd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eddd-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5eddd-123">INPUTS</span></span>

## <span data-ttu-id="5eddd-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5eddd-124">OUTPUTS</span></span>

### <span data-ttu-id="5eddd-125">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api202001.IVShellSite</span><span class="sxs-lookup"><span data-stu-id="5eddd-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="5eddd-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5eddd-126">NOTES</span></span>

<span data-ttu-id="5eddd-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5eddd-127">ALIASES</span></span>

## <span data-ttu-id="5eddd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5eddd-128">RELATED LINKS</span></span>


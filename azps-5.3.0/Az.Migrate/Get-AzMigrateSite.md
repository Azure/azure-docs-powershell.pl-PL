---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498958"
---
# <span data-ttu-id="50aa1-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="50aa1-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="50aa1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="50aa1-103">Metoda pobierania witryny.</span><span class="sxs-lookup"><span data-stu-id="50aa1-103">Method to get a site.</span></span>

## <span data-ttu-id="50aa1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50aa1-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="50aa1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="50aa1-106">Metoda pobierania witryny.</span><span class="sxs-lookup"><span data-stu-id="50aa1-106">Method to get a site.</span></span>

## <span data-ttu-id="50aa1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="50aa1-108">Przykład 1: Uzyskaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="50aa1-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="50aa1-109">Pobieranie witryny według nazwy</span><span class="sxs-lookup"><span data-stu-id="50aa1-109">Get site by name</span></span>

## <span data-ttu-id="50aa1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50aa1-110">PARAMETERS</span></span>

### <span data-ttu-id="50aa1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aa1-111">-DefaultProfile</span></span>
<span data-ttu-id="50aa1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50aa1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50aa1-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50aa1-113">-Name</span></span>
<span data-ttu-id="50aa1-114">Nazwa witryny.</span><span class="sxs-lookup"><span data-stu-id="50aa1-114">Site name.</span></span>

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

### <span data-ttu-id="50aa1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50aa1-115">-ResourceGroupName</span></span>
<span data-ttu-id="50aa1-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50aa1-116">The name of the resource group.</span></span>
<span data-ttu-id="50aa1-117">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="50aa1-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="50aa1-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="50aa1-118">-SubscriptionId</span></span>
<span data-ttu-id="50aa1-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="50aa1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="50aa1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aa1-120">CommonParameters</span></span>
<span data-ttu-id="50aa1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50aa1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aa1-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50aa1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aa1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50aa1-123">INPUTS</span></span>

## <span data-ttu-id="50aa1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50aa1-124">OUTPUTS</span></span>

### <span data-ttu-id="50aa1-125">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="50aa1-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="50aa1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50aa1-126">NOTES</span></span>

<span data-ttu-id="50aa1-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="50aa1-127">ALIASES</span></span>

## <span data-ttu-id="50aa1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50aa1-128">RELATED LINKS</span></span>


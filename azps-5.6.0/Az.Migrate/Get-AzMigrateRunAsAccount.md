---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982817"
---
# <span data-ttu-id="1e8f7-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="1e8f7-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="1e8f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8f7-103">Metoda uruchamiania jako konta.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-103">Method to get run as account.</span></span>

## <span data-ttu-id="1e8f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e8f7-104">SYNTAX</span></span>

### <span data-ttu-id="1e8f7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1e8f7-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1e8f7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1e8f7-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1e8f7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e8f7-107">DESCRIPTION</span></span>
<span data-ttu-id="1e8f7-108">Metoda uruchamiania jako konta.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-108">Method to get run as account.</span></span>

## <span data-ttu-id="1e8f7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e8f7-109">EXAMPLES</span></span>

### <span data-ttu-id="1e8f7-110">Przykład 1. Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1e8f7-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="1e8f7-111">Lista wszystkich kont w witrynie.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="1e8f7-112">Przykład 2. Pobierz</span><span class="sxs-lookup"><span data-stu-id="1e8f7-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="1e8f7-113">Uruchom jako konto według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-113">Get Run as account by name.</span></span>

## <span data-ttu-id="1e8f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e8f7-114">PARAMETERS</span></span>

### <span data-ttu-id="1e8f7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e8f7-115">-AccountName</span></span>
<span data-ttu-id="1e8f7-116">Uruchom jako nazwę ARM konta.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8f7-117">-DefaultProfile</span></span>
<span data-ttu-id="1e8f7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e8f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e8f7-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-120">The name of the resource group.</span></span>
<span data-ttu-id="1e8f7-121">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e8f7-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="1e8f7-122">-SiteName</span></span>
<span data-ttu-id="1e8f7-123">Nazwa witryny.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-123">Site name.</span></span>

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

### <span data-ttu-id="1e8f7-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e8f7-124">-SubscriptionId</span></span>
<span data-ttu-id="1e8f7-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1e8f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8f7-126">CommonParameters</span></span>
<span data-ttu-id="1e8f7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e8f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8f7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e8f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8f7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e8f7-129">INPUTS</span></span>

## <span data-ttu-id="1e8f7-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e8f7-130">OUTPUTS</span></span>

### <span data-ttu-id="1e8f7-131">Microsoft.Azure.PowerShell.Cmdlet.Migrate.Models.Api202001.IVCmdRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="1e8f7-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="1e8f7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e8f7-132">NOTES</span></span>

<span data-ttu-id="1e8f7-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1e8f7-133">ALIASES</span></span>

## <span data-ttu-id="1e8f7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e8f7-134">RELATED LINKS</span></span>


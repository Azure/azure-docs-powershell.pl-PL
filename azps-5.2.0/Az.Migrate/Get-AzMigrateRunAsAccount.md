---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369915"
---
# <span data-ttu-id="2c0ac-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="2c0ac-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="2c0ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0ac-103">Metoda uzyskiwania konta Uruchom jako.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-103">Method to get run as account.</span></span>

## <span data-ttu-id="2c0ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c0ac-104">SYNTAX</span></span>

### <span data-ttu-id="2c0ac-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2c0ac-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c0ac-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2c0ac-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2c0ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c0ac-107">DESCRIPTION</span></span>
<span data-ttu-id="2c0ac-108">Metoda uzyskiwania konta Uruchom jako.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-108">Method to get run as account.</span></span>

## <span data-ttu-id="2c0ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c0ac-109">EXAMPLES</span></span>

### <span data-ttu-id="2c0ac-110">Przykład 1: lista (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2c0ac-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="2c0ac-111">Wyświetlanie wszystkich kont Uruchom jako w witrynie.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="2c0ac-112">Przykład 2: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="2c0ac-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="2c0ac-113">Uzyskaj konto Uruchom jako według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-113">Get Run as account by name.</span></span>

## <span data-ttu-id="2c0ac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c0ac-114">PARAMETERS</span></span>

### <span data-ttu-id="2c0ac-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c0ac-115">-AccountName</span></span>
<span data-ttu-id="2c0ac-116">Nazwa RAMIENIa konta Uruchom jako.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="2c0ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0ac-117">-DefaultProfile</span></span>
<span data-ttu-id="2c0ac-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c0ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c0ac-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-120">The name of the resource group.</span></span>
<span data-ttu-id="2c0ac-121">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2c0ac-122">-Sitename</span><span class="sxs-lookup"><span data-stu-id="2c0ac-122">-SiteName</span></span>
<span data-ttu-id="2c0ac-123">Nazwa witryny.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-123">Site name.</span></span>

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

### <span data-ttu-id="2c0ac-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2c0ac-124">-SubscriptionId</span></span>
<span data-ttu-id="2c0ac-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2c0ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0ac-126">CommonParameters</span></span>
<span data-ttu-id="2c0ac-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0ac-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c0ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0ac-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c0ac-129">INPUTS</span></span>

## <span data-ttu-id="2c0ac-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c0ac-130">OUTPUTS</span></span>

### <span data-ttu-id="2c0ac-131">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="2c0ac-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="2c0ac-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c0ac-132">NOTES</span></span>

<span data-ttu-id="2c0ac-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2c0ac-133">ALIASES</span></span>

## <span data-ttu-id="2c0ac-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c0ac-134">RELATED LINKS</span></span>


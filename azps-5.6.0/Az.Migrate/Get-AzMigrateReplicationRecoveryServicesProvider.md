---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982833"
---
# <span data-ttu-id="1b9fd-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1b9fd-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="1b9fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9fd-103">Pobiera szczegółowe informacje o zarejestrowanym dostawcy usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="1b9fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b9fd-104">SYNTAX</span></span>

### <span data-ttu-id="1b9fd-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1b9fd-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b9fd-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1b9fd-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b9fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b9fd-107">DESCRIPTION</span></span>
<span data-ttu-id="1b9fd-108">Pobiera szczegółowe informacje o zarejestrowanym dostawcy usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="1b9fd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b9fd-109">EXAMPLES</span></span>

### <span data-ttu-id="1b9fd-110">Przykład 1. Uzyskiwanie wszystkich dostawców w magazynie</span><span class="sxs-lookup"><span data-stu-id="1b9fd-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="1b9fd-111">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-111">List all.</span></span>

## <span data-ttu-id="1b9fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b9fd-112">PARAMETERS</span></span>

### <span data-ttu-id="1b9fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9fd-113">-DefaultProfile</span></span>
<span data-ttu-id="1b9fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b9fd-115">- FabricName</span><span class="sxs-lookup"><span data-stu-id="1b9fd-115">-FabricName</span></span>
<span data-ttu-id="1b9fd-116">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-116">Fabric name.</span></span>

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

### <span data-ttu-id="1b9fd-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="1b9fd-117">-ProviderName</span></span>
<span data-ttu-id="1b9fd-118">Nazwa dostawcy usług odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="1b9fd-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="1b9fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b9fd-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1b9fd-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1b9fd-121">-ResourceName</span></span>
<span data-ttu-id="1b9fd-122">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="1b9fd-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b9fd-123">-SubscriptionId</span></span>
<span data-ttu-id="1b9fd-124">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1b9fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9fd-125">CommonParameters</span></span>
<span data-ttu-id="1b9fd-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9fd-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b9fd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9fd-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b9fd-128">INPUTS</span></span>

## <span data-ttu-id="1b9fd-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b9fd-129">OUTPUTS</span></span>

### <span data-ttu-id="1b9fd-130">Microsoft.Azure.PowerShell.Cmdlet.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1b9fd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="1b9fd-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b9fd-131">NOTES</span></span>

<span data-ttu-id="1b9fd-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1b9fd-132">ALIASES</span></span>

## <span data-ttu-id="1b9fd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b9fd-133">RELATED LINKS</span></span>


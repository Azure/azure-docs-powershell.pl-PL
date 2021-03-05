---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 261d7467d67708380f86c8df061fdda02eb095c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982922"
---
# <span data-ttu-id="34f54-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="34f54-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="34f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f54-102">SYNOPSIS</span></span>
<span data-ttu-id="34f54-103">Pobiera szczegółowe informacje dotyczące zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="34f54-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="34f54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34f54-104">SYNTAX</span></span>

### <span data-ttu-id="34f54-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="34f54-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34f54-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="34f54-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="34f54-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="34f54-107">DESCRIPTION</span></span>
<span data-ttu-id="34f54-108">Pobiera szczegółowe informacje dotyczące zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="34f54-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="34f54-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34f54-109">EXAMPLES</span></span>

### <span data-ttu-id="34f54-110">Przykład 1. Pobierz wszystkie zasady w magazynie</span><span class="sxs-lookup"><span data-stu-id="34f54-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="34f54-111">Pobierz wszystkie zasady.</span><span class="sxs-lookup"><span data-stu-id="34f54-111">Get all policies.</span></span>

### <span data-ttu-id="34f54-112">Przykład 2. Uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="34f54-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="34f54-113">Uzyskaj konkretny.</span><span class="sxs-lookup"><span data-stu-id="34f54-113">Get a specific one.</span></span>

## <span data-ttu-id="34f54-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f54-114">PARAMETERS</span></span>

### <span data-ttu-id="34f54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f54-115">-DefaultProfile</span></span>
<span data-ttu-id="34f54-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34f54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f54-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="34f54-117">-PolicyName</span></span>
<span data-ttu-id="34f54-118">Nazwa zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="34f54-118">Replication policy name.</span></span>

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

### <span data-ttu-id="34f54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f54-119">-ResourceGroupName</span></span>
<span data-ttu-id="34f54-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="34f54-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="34f54-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="34f54-121">-ResourceName</span></span>
<span data-ttu-id="34f54-122">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="34f54-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="34f54-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34f54-123">-SubscriptionId</span></span>
<span data-ttu-id="34f54-124">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="34f54-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="34f54-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f54-125">CommonParameters</span></span>
<span data-ttu-id="34f54-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f54-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f54-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f54-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f54-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34f54-128">INPUTS</span></span>

## <span data-ttu-id="34f54-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34f54-129">OUTPUTS</span></span>

### <span data-ttu-id="34f54-130">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iPolicy</span><span class="sxs-lookup"><span data-stu-id="34f54-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="34f54-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34f54-131">NOTES</span></span>

<span data-ttu-id="34f54-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="34f54-132">ALIASES</span></span>

## <span data-ttu-id="34f54-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34f54-133">RELATED LINKS</span></span>


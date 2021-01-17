---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342838"
---
# <span data-ttu-id="103f7-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="103f7-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="103f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="103f7-102">SYNOPSIS</span></span>
<span data-ttu-id="103f7-103">Pobiera szczegóły zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="103f7-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="103f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="103f7-104">SYNTAX</span></span>

### <span data-ttu-id="103f7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="103f7-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="103f7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="103f7-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="103f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="103f7-107">DESCRIPTION</span></span>
<span data-ttu-id="103f7-108">Pobiera szczegóły zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="103f7-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="103f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="103f7-109">EXAMPLES</span></span>

### <span data-ttu-id="103f7-110">Przykład 1: pobieranie wszystkich zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="103f7-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="103f7-111">Pobierz wszystkie zasady.</span><span class="sxs-lookup"><span data-stu-id="103f7-111">Get all policies.</span></span>

### <span data-ttu-id="103f7-112">Przykład 2: uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="103f7-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="103f7-113">Uzyskaj określoną osobę.</span><span class="sxs-lookup"><span data-stu-id="103f7-113">Get a specific one.</span></span>

## <span data-ttu-id="103f7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="103f7-114">PARAMETERS</span></span>

### <span data-ttu-id="103f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103f7-115">-DefaultProfile</span></span>
<span data-ttu-id="103f7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="103f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="103f7-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="103f7-117">-PolicyName</span></span>
<span data-ttu-id="103f7-118">Nazwa zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="103f7-118">Replication policy name.</span></span>

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

### <span data-ttu-id="103f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="103f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="103f7-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="103f7-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="103f7-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="103f7-121">-ResourceName</span></span>
<span data-ttu-id="103f7-122">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="103f7-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="103f7-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="103f7-123">-SubscriptionId</span></span>
<span data-ttu-id="103f7-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="103f7-124">The subscription Id.</span></span>

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

### <span data-ttu-id="103f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103f7-125">CommonParameters</span></span>
<span data-ttu-id="103f7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103f7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="103f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103f7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="103f7-128">INPUTS</span></span>

## <span data-ttu-id="103f7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="103f7-129">OUTPUTS</span></span>

### <span data-ttu-id="103f7-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="103f7-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="103f7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="103f7-131">NOTES</span></span>

<span data-ttu-id="103f7-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="103f7-132">ALIASES</span></span>

## <span data-ttu-id="103f7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="103f7-133">RELATED LINKS</span></span>


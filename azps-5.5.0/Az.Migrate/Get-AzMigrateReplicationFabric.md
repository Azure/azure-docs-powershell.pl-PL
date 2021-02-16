---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 6872eb3da4f67969dcb6ec57a9e300677bd4611b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190186"
---
# <span data-ttu-id="e1ae0-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="e1ae0-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="e1ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ae0-103">Pobiera szczegółowe informacje na temat struktury azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="e1ae0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1ae0-104">SYNTAX</span></span>

### <span data-ttu-id="e1ae0-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e1ae0-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1ae0-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e1ae0-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e1ae0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1ae0-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ae0-108">Pobiera szczegółowe informacje na temat struktury azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="e1ae0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1ae0-109">EXAMPLES</span></span>

### <span data-ttu-id="e1ae0-110">Przykład 1. Wszystkie zasoby są podszyte według grupy zasobów i nazwy magazynu</span><span class="sxs-lookup"><span data-stu-id="e1ae0-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="e1ae0-111">Wszystko, co należy chcieć w grupie zasobów i magazynie</span><span class="sxs-lookup"><span data-stu-id="e1ae0-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="e1ae0-112">Przykład 2. Uzyskiwanie struktury według grupy zasobów, nazwy magazynu i nazwy tkaniny</span><span class="sxs-lookup"><span data-stu-id="e1ae0-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="e1ae0-113">Uzyskaj konkretną tkaninę</span><span class="sxs-lookup"><span data-stu-id="e1ae0-113">Get a specific fabric</span></span>

## <span data-ttu-id="e1ae0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1ae0-114">PARAMETERS</span></span>

### <span data-ttu-id="e1ae0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ae0-115">-DefaultProfile</span></span>
<span data-ttu-id="e1ae0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ae0-117">- FabricName</span><span class="sxs-lookup"><span data-stu-id="e1ae0-117">-FabricName</span></span>
<span data-ttu-id="e1ae0-118">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-118">Fabric name.</span></span>

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

### <span data-ttu-id="e1ae0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ae0-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1ae0-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e1ae0-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e1ae0-121">-ResourceName</span></span>
<span data-ttu-id="e1ae0-122">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e1ae0-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1ae0-123">-SubscriptionId</span></span>
<span data-ttu-id="e1ae0-124">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e1ae0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ae0-125">CommonParameters</span></span>
<span data-ttu-id="e1ae0-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ae0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ae0-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ae0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ae0-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ae0-128">INPUTS</span></span>

## <span data-ttu-id="e1ae0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ae0-129">OUTPUTS</span></span>

### <span data-ttu-id="e1ae0-130">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iFabric</span><span class="sxs-lookup"><span data-stu-id="e1ae0-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="e1ae0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1ae0-131">NOTES</span></span>

<span data-ttu-id="e1ae0-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e1ae0-132">ALIASES</span></span>

## <span data-ttu-id="e1ae0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1ae0-133">RELATED LINKS</span></span>


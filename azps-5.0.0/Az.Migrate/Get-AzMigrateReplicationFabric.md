---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234539"
---
# <span data-ttu-id="e15a8-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="e15a8-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="e15a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e15a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e15a8-103">Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e15a8-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="e15a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e15a8-104">SYNTAX</span></span>

### <span data-ttu-id="e15a8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e15a8-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e15a8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e15a8-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e15a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e15a8-107">DESCRIPTION</span></span>
<span data-ttu-id="e15a8-108">Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e15a8-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="e15a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e15a8-109">EXAMPLES</span></span>

### <span data-ttu-id="e15a8-110">Przykład 1. Pobierz wszystkie materiały szkieletowe według grupy zasobów i nazwy magazynu</span><span class="sxs-lookup"><span data-stu-id="e15a8-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="e15a8-111">Pobieranie całej sieci szkieletowej w grupie zasobów i magazynie</span><span class="sxs-lookup"><span data-stu-id="e15a8-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="e15a8-112">Przykład 2: pobieranie sieci szkieletowej według grup zasobów, nazwy i nazwy magazynu</span><span class="sxs-lookup"><span data-stu-id="e15a8-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="e15a8-113">Uzyskiwanie określonego szkieletu</span><span class="sxs-lookup"><span data-stu-id="e15a8-113">Get a specific fabric</span></span>

## <span data-ttu-id="e15a8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e15a8-114">PARAMETERS</span></span>

### <span data-ttu-id="e15a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e15a8-115">-DefaultProfile</span></span>
<span data-ttu-id="e15a8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e15a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e15a8-117">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="e15a8-117">-FabricName</span></span>
<span data-ttu-id="e15a8-118">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="e15a8-118">Fabric name.</span></span>

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

### <span data-ttu-id="e15a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e15a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="e15a8-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e15a8-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e15a8-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e15a8-121">-ResourceName</span></span>
<span data-ttu-id="e15a8-122">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e15a8-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e15a8-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e15a8-123">-SubscriptionId</span></span>
<span data-ttu-id="e15a8-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e15a8-124">The subscription Id.</span></span>

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

### <span data-ttu-id="e15a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15a8-125">CommonParameters</span></span>
<span data-ttu-id="e15a8-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e15a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15a8-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e15a8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15a8-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e15a8-128">INPUTS</span></span>

## <span data-ttu-id="e15a8-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e15a8-129">OUTPUTS</span></span>

### <span data-ttu-id="e15a8-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="e15a8-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="e15a8-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e15a8-131">NOTES</span></span>

<span data-ttu-id="e15a8-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e15a8-132">ALIASES</span></span>

## <span data-ttu-id="e15a8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e15a8-133">RELATED LINKS</span></span>


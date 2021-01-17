---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330829"
---
# <span data-ttu-id="553b3-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="553b3-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="553b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="553b3-102">SYNOPSIS</span></span>
<span data-ttu-id="553b3-103">Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="553b3-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="553b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="553b3-104">SYNTAX</span></span>

### <span data-ttu-id="553b3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="553b3-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="553b3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="553b3-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="553b3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="553b3-107">DESCRIPTION</span></span>
<span data-ttu-id="553b3-108">Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="553b3-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="553b3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="553b3-109">EXAMPLES</span></span>

### <span data-ttu-id="553b3-110">Przykład 1. Pobierz wszystkie materiały szkieletowe według grupy zasobów i nazwy magazynu</span><span class="sxs-lookup"><span data-stu-id="553b3-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="553b3-111">Pobieranie całej sieci szkieletowej w grupie zasobów i magazynie</span><span class="sxs-lookup"><span data-stu-id="553b3-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="553b3-112">Przykład 2: pobieranie sieci szkieletowej według grup zasobów, nazwy i nazwy magazynu</span><span class="sxs-lookup"><span data-stu-id="553b3-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="553b3-113">Uzyskiwanie określonego szkieletu</span><span class="sxs-lookup"><span data-stu-id="553b3-113">Get a specific fabric</span></span>

## <span data-ttu-id="553b3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="553b3-114">PARAMETERS</span></span>

### <span data-ttu-id="553b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553b3-115">-DefaultProfile</span></span>
<span data-ttu-id="553b3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="553b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="553b3-117">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="553b3-117">-FabricName</span></span>
<span data-ttu-id="553b3-118">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="553b3-118">Fabric name.</span></span>

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

### <span data-ttu-id="553b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="553b3-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="553b3-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="553b3-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="553b3-121">-ResourceName</span></span>
<span data-ttu-id="553b3-122">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="553b3-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="553b3-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="553b3-123">-SubscriptionId</span></span>
<span data-ttu-id="553b3-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="553b3-124">The subscription Id.</span></span>

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

### <span data-ttu-id="553b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553b3-125">CommonParameters</span></span>
<span data-ttu-id="553b3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553b3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="553b3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553b3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="553b3-128">INPUTS</span></span>

## <span data-ttu-id="553b3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="553b3-129">OUTPUTS</span></span>

### <span data-ttu-id="553b3-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="553b3-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="553b3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="553b3-131">NOTES</span></span>

<span data-ttu-id="553b3-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="553b3-132">ALIASES</span></span>

## <span data-ttu-id="553b3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="553b3-133">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490138"
---
# <span data-ttu-id="13c79-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="13c79-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="13c79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13c79-102">SYNOPSIS</span></span>
<span data-ttu-id="13c79-103">Umożliwia wyświetlenie szczegółów zarejestrowanego dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="13c79-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="13c79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13c79-104">SYNTAX</span></span>

### <span data-ttu-id="13c79-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="13c79-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="13c79-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="13c79-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="13c79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13c79-107">DESCRIPTION</span></span>
<span data-ttu-id="13c79-108">Umożliwia wyświetlenie szczegółów zarejestrowanego dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="13c79-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="13c79-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13c79-109">EXAMPLES</span></span>

### <span data-ttu-id="13c79-110">Przykład 1: Uzyskaj wszystkich dostawców w magazynie</span><span class="sxs-lookup"><span data-stu-id="13c79-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="13c79-111">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="13c79-111">List all.</span></span>

## <span data-ttu-id="13c79-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13c79-112">PARAMETERS</span></span>

### <span data-ttu-id="13c79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c79-113">-DefaultProfile</span></span>
<span data-ttu-id="13c79-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13c79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c79-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="13c79-115">-FabricName</span></span>
<span data-ttu-id="13c79-116">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="13c79-116">Fabric name.</span></span>

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

### <span data-ttu-id="13c79-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="13c79-117">-ProviderName</span></span>
<span data-ttu-id="13c79-118">Nazwa dostawcy usług Recovery Services</span><span class="sxs-lookup"><span data-stu-id="13c79-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="13c79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c79-119">-ResourceGroupName</span></span>
<span data-ttu-id="13c79-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="13c79-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="13c79-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="13c79-121">-ResourceName</span></span>
<span data-ttu-id="13c79-122">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="13c79-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="13c79-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="13c79-123">-SubscriptionId</span></span>
<span data-ttu-id="13c79-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="13c79-124">The subscription Id.</span></span>

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

### <span data-ttu-id="13c79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c79-125">CommonParameters</span></span>
<span data-ttu-id="13c79-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c79-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13c79-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c79-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13c79-128">INPUTS</span></span>

## <span data-ttu-id="13c79-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13c79-129">OUTPUTS</span></span>

### <span data-ttu-id="13c79-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="13c79-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="13c79-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13c79-131">NOTES</span></span>

<span data-ttu-id="13c79-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="13c79-132">ALIASES</span></span>

## <span data-ttu-id="13c79-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13c79-133">RELATED LINKS</span></span>


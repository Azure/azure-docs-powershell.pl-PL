---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234531"
---
# <span data-ttu-id="a4b0b-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4b0b-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="a4b0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b0b-103">Umożliwia wyświetlenie szczegółów zarejestrowanego dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="a4b0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4b0b-104">SYNTAX</span></span>

### <span data-ttu-id="a4b0b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a4b0b-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4b0b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a4b0b-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b0b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a4b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="a4b0b-108">Umożliwia wyświetlenie szczegółów zarejestrowanego dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="a4b0b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="a4b0b-110">Przykład 1: Uzyskaj wszystkich dostawców w magazynie</span><span class="sxs-lookup"><span data-stu-id="a4b0b-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="a4b0b-111">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-111">List all.</span></span>

## <span data-ttu-id="a4b0b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="a4b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="a4b0b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b0b-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="a4b0b-115">-FabricName</span></span>
<span data-ttu-id="a4b0b-116">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-116">Fabric name.</span></span>

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

### <span data-ttu-id="a4b0b-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="a4b0b-117">-ProviderName</span></span>
<span data-ttu-id="a4b0b-118">Nazwa dostawcy usług Recovery Services</span><span class="sxs-lookup"><span data-stu-id="a4b0b-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="a4b0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4b0b-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a4b0b-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a4b0b-121">-ResourceName</span></span>
<span data-ttu-id="a4b0b-122">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a4b0b-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a4b0b-123">-SubscriptionId</span></span>
<span data-ttu-id="a4b0b-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-124">The subscription Id.</span></span>

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

### <span data-ttu-id="a4b0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b0b-125">CommonParameters</span></span>
<span data-ttu-id="a4b0b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b0b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b0b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b0b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4b0b-128">INPUTS</span></span>

## <span data-ttu-id="a4b0b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4b0b-129">OUTPUTS</span></span>

### <span data-ttu-id="a4b0b-130">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4b0b-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="a4b0b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4b0b-131">NOTES</span></span>

<span data-ttu-id="a4b0b-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a4b0b-132">ALIASES</span></span>

## <span data-ttu-id="a4b0b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4b0b-133">RELATED LINKS</span></span>


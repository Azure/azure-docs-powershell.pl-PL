---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716894"
---
# <span data-ttu-id="d33b6-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d33b6-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d33b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d33b6-102">SYNOPSIS</span></span>
<span data-ttu-id="d33b6-103">Tworzy plan odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="d33b6-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d33b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d33b6-104">SYNTAX</span></span>

### <span data-ttu-id="d33b6-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d33b6-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d33b6-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d33b6-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d33b6-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="d33b6-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d33b6-108">DESCRIPTION</span></span>
<span data-ttu-id="d33b6-109">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** tworzy plan odzyskiwania odzyskiwania witryny Azure w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d33b6-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="d33b6-110">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych należących do danej aplikacji w jednostce w celu umożliwienia ich odzyskania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="d33b6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d33b6-111">EXAMPLES</span></span>

### <span data-ttu-id="d33b6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d33b6-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="d33b6-113">Rozpoczyna operację tworzenia planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d33b6-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d33b6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d33b6-114">PARAMETERS</span></span>

### <span data-ttu-id="d33b6-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="d33b6-115">-Azure</span></span>
<span data-ttu-id="d33b6-116">Parametr Przełącz określający, czy Lokalizacja odzyskiwania planu odzyskiwania to Azure.</span><span class="sxs-lookup"><span data-stu-id="d33b6-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="d33b6-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="d33b6-118">Określa model wdrożenia trybu failover (klasyczny lub Menedżer zasobów) elementów chronionych replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d33b6-119">-Name</span></span>
<span data-ttu-id="d33b6-120">Nazwa planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-121">-Path</span><span class="sxs-lookup"><span data-stu-id="d33b6-121">-Path</span></span>
<span data-ttu-id="d33b6-122">Określa ścieżkę do pliku JSON definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="d33b6-123">Za pomocą notacji JSON z definicji planu odzyskiwania można utworzyć plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="d33b6-124">-PrimaryFabric</span></span>
<span data-ttu-id="d33b6-125">Określa obiekt sieci szkieletowej ASR dla podstawowej sieci szkieletowej ASR elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="d33b6-126">-RecoveryFabric</span></span>
<span data-ttu-id="d33b6-127">Określa obiekt sieci szkieletowej ASR dla odtwarzania ASR z elementami chronionymi replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d33b6-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d33b6-129">Lista elementów chronionych replikacji, które mają zostać dodane do pierwszej grupy planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d33b6-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d33b6-130">-Confirm</span></span>
<span data-ttu-id="d33b6-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d33b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33b6-132">-WhatIf</span></span>
<span data-ttu-id="d33b6-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d33b6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d33b6-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d33b6-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33b6-135">CommonParameters</span></span>
<span data-ttu-id="d33b6-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33b6-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33b6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33b6-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d33b6-138">INPUTS</span></span>

### <span data-ttu-id="d33b6-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="d33b6-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="d33b6-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d33b6-140">OUTPUTS</span></span>

### <span data-ttu-id="d33b6-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="d33b6-141">System.Object</span></span>

## <span data-ttu-id="d33b6-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d33b6-142">NOTES</span></span>

## <span data-ttu-id="d33b6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d33b6-143">RELATED LINKS</span></span>

[<span data-ttu-id="d33b6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d33b6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d33b6-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d33b6-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d33b6-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d33b6-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)



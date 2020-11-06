---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: ceedd758a660828ed3ee93390384c1e212c55097
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524309"
---
# <span data-ttu-id="6e8d2-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8d2-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6e8d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8d2-103">Tworzy plan odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e8d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e8d2-104">SYNTAX</span></span>

### <span data-ttu-id="6e8d2-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e8d2-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8d2-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6e8d2-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8d2-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6e8d2-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8d2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6e8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="6e8d2-109">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrRecoveryPlan** tworzy plan odzyskiwania odzyskiwania witryny Azure w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="6e8d2-110">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych należących do danej aplikacji w jednostce w celu umożliwienia ich odzyskania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="6e8d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e8d2-111">EXAMPLES</span></span>

### <span data-ttu-id="6e8d2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e8d2-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="6e8d2-113">Rozpoczyna operację tworzenia planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6e8d2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e8d2-114">PARAMETERS</span></span>

### <span data-ttu-id="6e8d2-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="6e8d2-115">-Azure</span></span>
<span data-ttu-id="6e8d2-116">Parametr Przełącz określający, czy Lokalizacja odzyskiwania planu odzyskiwania to Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8d2-117">-DefaultProfile</span></span>
<span data-ttu-id="6e8d2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="6e8d2-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="6e8d2-120">Określa model wdrożenia trybu failover (klasyczny lub Menedżer zasobów) elementów chronionych replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e8d2-121">-Name</span></span>
<span data-ttu-id="6e8d2-122">Nazwa planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-123">-Path</span><span class="sxs-lookup"><span data-stu-id="6e8d2-123">-Path</span></span>
<span data-ttu-id="6e8d2-124">Określa ścieżkę do pliku JSON definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="6e8d2-125">Za pomocą notacji JSON z definicji planu odzyskiwania można utworzyć plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="6e8d2-126">-PrimaryFabric</span></span>
<span data-ttu-id="6e8d2-127">Określa obiekt sieci szkieletowej ASR dla podstawowej sieci szkieletowej ASR elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6e8d2-128">-RecoveryFabric</span></span>
<span data-ttu-id="6e8d2-129">Określa obiekt sieci szkieletowej ASR dla odtwarzania ASR z elementami chronionymi replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6e8d2-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6e8d2-131">Lista elementów chronionych replikacji, które mają zostać dodane do pierwszej grupy planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e8d2-132">-Confirm</span></span>
<span data-ttu-id="6e8d2-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8d2-134">-WhatIf</span></span>
<span data-ttu-id="6e8d2-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e8d2-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8d2-137">CommonParameters</span></span>
<span data-ttu-id="6e8d2-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8d2-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8d2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8d2-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e8d2-140">INPUTS</span></span>

### <span data-ttu-id="6e8d2-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="6e8d2-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="6e8d2-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e8d2-142">OUTPUTS</span></span>

### <span data-ttu-id="6e8d2-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="6e8d2-143">System.Object</span></span>

## <span data-ttu-id="6e8d2-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e8d2-144">NOTES</span></span>

## <span data-ttu-id="6e8d2-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e8d2-145">RELATED LINKS</span></span>

[<span data-ttu-id="6e8d2-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8d2-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6e8d2-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8d2-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6e8d2-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6e8d2-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)



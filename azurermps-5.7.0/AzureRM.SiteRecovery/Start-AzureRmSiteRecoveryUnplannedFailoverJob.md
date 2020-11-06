---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524893"
---
# <span data-ttu-id="6368f-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6368f-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="6368f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6368f-102">SYNOPSIS</span></span>
<span data-ttu-id="6368f-103">Rozpoczyna nieplanowaną pracę awaryjną dla jednostki ochrony odzyskiwania witryny lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6368f-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6368f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6368f-104">SYNTAX</span></span>

### <span data-ttu-id="6368f-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6368f-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6368f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6368f-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6368f-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="6368f-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6368f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6368f-108">DESCRIPTION</span></span>
<span data-ttu-id="6368f-109">Polecenie cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** uruchamia nieplanowaną pracę awaryjną w trybie failover jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6368f-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="6368f-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmSiteRecoveryJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6368f-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="6368f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6368f-111">EXAMPLES</span></span>

## <span data-ttu-id="6368f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6368f-112">PARAMETERS</span></span>

### <span data-ttu-id="6368f-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6368f-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6368f-114">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6368f-114">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6368f-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6368f-116">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6368f-116">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6368f-117">-DefaultProfile</span></span>
<span data-ttu-id="6368f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6368f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="6368f-119">-Direction</span></span>
<span data-ttu-id="6368f-120">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="6368f-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="6368f-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6368f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6368f-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6368f-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="6368f-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6368f-123">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="6368f-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="6368f-125">Wskazuje, że akcja może wykonać operacje witryny źródłowej.</span><span class="sxs-lookup"><span data-stu-id="6368f-125">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6368f-126">-ProtectionEntity</span></span>
<span data-ttu-id="6368f-127">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="6368f-127">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6368f-128">-RecoveryPlan</span></span>
<span data-ttu-id="6368f-129">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6368f-129">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6368f-130">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6368f-131">CommonParameters</span></span>
<span data-ttu-id="6368f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6368f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6368f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6368f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6368f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6368f-134">INPUTS</span></span>

### <span data-ttu-id="6368f-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6368f-135">ASRProtectionEntity</span></span>
<span data-ttu-id="6368f-136">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6368f-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="6368f-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6368f-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="6368f-138">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6368f-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="6368f-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6368f-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="6368f-140">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6368f-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="6368f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6368f-141">OUTPUTS</span></span>

### <span data-ttu-id="6368f-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6368f-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6368f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6368f-143">NOTES</span></span>

## <span data-ttu-id="6368f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6368f-144">RELATED LINKS</span></span>

[<span data-ttu-id="6368f-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="6368f-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)



---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526562"
---
# <span data-ttu-id="47f18-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="47f18-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="47f18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47f18-102">SYNOPSIS</span></span>
<span data-ttu-id="47f18-103">Rozpoczyna test pracy awaryjnej jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="47f18-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47f18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47f18-104">SYNTAX</span></span>

### <span data-ttu-id="47f18-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47f18-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="47f18-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="47f18-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="47f18-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="47f18-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="47f18-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="47f18-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="47f18-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47f18-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="47f18-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47f18-114">Opis</span><span class="sxs-lookup"><span data-stu-id="47f18-114">DESCRIPTION</span></span>
<span data-ttu-id="47f18-115">Polecenie cmdlet **Start-AzureRmSiteRecoveryTestFailoverJob** rozpoczyna test pracy awaryjnej jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="47f18-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="47f18-116">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmSiteRecoveryJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f18-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="47f18-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47f18-117">EXAMPLES</span></span>

## <span data-ttu-id="47f18-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47f18-118">PARAMETERS</span></span>

### <span data-ttu-id="47f18-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="47f18-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="47f18-120">Określa identyfikator sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47f18-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f18-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="47f18-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="47f18-122">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47f18-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="47f18-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="47f18-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="47f18-124">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="47f18-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="47f18-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f18-125">-DefaultProfile</span></span>
<span data-ttu-id="47f18-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47f18-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47f18-127">-Direction</span><span class="sxs-lookup"><span data-stu-id="47f18-127">-Direction</span></span>
<span data-ttu-id="47f18-128">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="47f18-128">Specifies the failover direction.</span></span>
<span data-ttu-id="47f18-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="47f18-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47f18-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="47f18-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="47f18-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="47f18-131">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="47f18-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="47f18-132">-ProtectionEntity</span></span>
<span data-ttu-id="47f18-133">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="47f18-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47f18-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47f18-134">-RecoveryPlan</span></span>
<span data-ttu-id="47f18-135">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="47f18-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47f18-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47f18-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47f18-137">-Sieć VMNetwork</span><span class="sxs-lookup"><span data-stu-id="47f18-137">-VMNetwork</span></span>
<span data-ttu-id="47f18-138">Określa sieć maszyny wirtualnej odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="47f18-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f18-139">CommonParameters</span></span>
<span data-ttu-id="47f18-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f18-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47f18-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f18-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47f18-142">INPUTS</span></span>

### <span data-ttu-id="47f18-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="47f18-143">ASRProtectionEntity</span></span>
<span data-ttu-id="47f18-144">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="47f18-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="47f18-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47f18-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="47f18-146">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="47f18-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="47f18-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47f18-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="47f18-148">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="47f18-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="47f18-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47f18-149">OUTPUTS</span></span>

### <span data-ttu-id="47f18-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="47f18-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="47f18-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47f18-151">NOTES</span></span>

## <span data-ttu-id="47f18-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47f18-152">RELATED LINKS</span></span>

[<span data-ttu-id="47f18-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="47f18-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

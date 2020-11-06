---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543075"
---
# <span data-ttu-id="3235e-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3235e-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="3235e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3235e-102">SYNOPSIS</span></span>
<span data-ttu-id="3235e-103">Włączanie replikacji elementu chronionego przed ASR przez utworzenie elementu chronionego replikacji</span><span class="sxs-lookup"><span data-stu-id="3235e-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3235e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3235e-104">SYNTAX</span></span>

### <span data-ttu-id="3235e-105">DisableD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3235e-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3235e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3235e-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3235e-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3235e-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3235e-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="3235e-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3235e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3235e-109">DESCRIPTION</span></span>
<span data-ttu-id="3235e-110">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="3235e-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="3235e-111">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego przed ASR.</span><span class="sxs-lookup"><span data-stu-id="3235e-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="3235e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3235e-112">EXAMPLES</span></span>

### <span data-ttu-id="3235e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3235e-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="3235e-114">Rozpoczyna operację tworzenia chronionego elementu replikacji dla określonego elementu do ochrony przed ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3235e-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3235e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3235e-115">PARAMETERS</span></span>

### <span data-ttu-id="3235e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3235e-116">-Name</span></span>
<span data-ttu-id="3235e-117">Określa nazwę elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="3235e-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-118">-OS</span><span class="sxs-lookup"><span data-stu-id="3235e-118">-OS</span></span>
<span data-ttu-id="3235e-119">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="3235e-119">Specifies the operating system family.</span></span>
<span data-ttu-id="3235e-120">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="3235e-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="3235e-121">-OSDiskName</span></span>
<span data-ttu-id="3235e-122">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="3235e-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3235e-123">-ProtectableItem</span></span>
<span data-ttu-id="3235e-124">Określa obiekt elementu umożliwiającego ochronę przed ASR, dla którego jest włączana replikacja.</span><span class="sxs-lookup"><span data-stu-id="3235e-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3235e-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="3235e-126">Określa obiekt mapowania kontenera ochrony przed Autoodzyskiwaniem odpowiadający zasadom replikacji, które mają być używane do replikacji.</span><span class="sxs-lookup"><span data-stu-id="3235e-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3235e-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3235e-128">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="3235e-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3235e-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="3235e-130">Określa identyfikator ARM grupy zasobów, w której maszyna wirtualna zostanie utworzona w przypadku przełączenia w tryb pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3235e-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3235e-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3235e-131">-WaitForCompletion</span></span>
<span data-ttu-id="3235e-132">Określa, że polecenie cmdlet powinno czekać na ukończenie operacji przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="3235e-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="3235e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3235e-133">-Confirm</span></span>
<span data-ttu-id="3235e-134">Monituje o potwierdzenie przed rozpoczęciem operacji.</span><span class="sxs-lookup"><span data-stu-id="3235e-134">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="3235e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3235e-135">-WhatIf</span></span>
<span data-ttu-id="3235e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3235e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3235e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3235e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3235e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3235e-138">CommonParameters</span></span>
<span data-ttu-id="3235e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3235e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3235e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3235e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3235e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3235e-141">INPUTS</span></span>

### <span data-ttu-id="3235e-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3235e-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="3235e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3235e-143">OUTPUTS</span></span>

### <span data-ttu-id="3235e-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3235e-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3235e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3235e-145">NOTES</span></span>

## <span data-ttu-id="3235e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3235e-146">RELATED LINKS</span></span>

[<span data-ttu-id="3235e-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3235e-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3235e-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3235e-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3235e-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3235e-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 50015893c3bbd45196e4dde24088fe3ce8b595c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718722"
---
# <span data-ttu-id="2cbd7-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cbd7-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="2cbd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbd7-103">Zmienia punkt odzyskiwania dla uszkodzonego elementu chronionego przed zatwierdzeniem operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cbd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cbd7-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbd7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2cbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="2cbd7-106">**Uruchomienie programu AzureRmRecoveryServicesAsrApplyRecoveryPoint** powoduje zmianę punktu odzyskiwania dla elementu chronionego niepowodzeniem przed zatwierdzeniem operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="2cbd7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cbd7-107">EXAMPLES</span></span>

### <span data-ttu-id="2cbd7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2cbd7-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="2cbd7-109">Rozpoczyna stosowanie określonego punktu odzyskiwania do elementu chronionego replikacji i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2cbd7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cbd7-110">PARAMETERS</span></span>

### <span data-ttu-id="2cbd7-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2cbd7-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="2cbd7-112">Określa podstawowy plik certyfikatu, jeśli jest używane szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="2cbd7-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2cbd7-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="2cbd7-114">Określa pomocniczy plik certyfikatu, jeśli jest używany szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="2cbd7-115">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cbd7-115">-RecoveryPoint</span></span>
<span data-ttu-id="2cbd7-116">Określa obiekt punktu odzyskiwania odpowiadający punktowi odzyskiwania, który ma zostać zastosowany.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-116">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd7-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2cbd7-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2cbd7-118">Określa obiekt elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-118">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cbd7-119">-Confirm</span></span>
<span data-ttu-id="2cbd7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbd7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbd7-121">-WhatIf</span></span>
<span data-ttu-id="2cbd7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cbd7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbd7-124">CommonParameters</span></span>
<span data-ttu-id="2cbd7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbd7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbd7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbd7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cbd7-127">INPUTS</span></span>

### <span data-ttu-id="2cbd7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2cbd7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2cbd7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cbd7-129">OUTPUTS</span></span>

### <span data-ttu-id="2cbd7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2cbd7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2cbd7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cbd7-131">NOTES</span></span>

## <span data-ttu-id="2cbd7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cbd7-132">RELATED LINKS</span></span>

[<span data-ttu-id="2cbd7-133">Polecenia cmdlet dotyczące odzyskiwania witryny Azure Site</span><span class="sxs-lookup"><span data-stu-id="2cbd7-133">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)

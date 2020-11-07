---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: d669e450e096e4d9c0c61a3e1d485e3caaaa9ae3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886610"
---
# <span data-ttu-id="ac757-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ac757-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="ac757-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac757-102">SYNOPSIS</span></span>
<span data-ttu-id="ac757-103">Zmienia punkt odzyskiwania elementu chronionego przed przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ac757-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="ac757-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac757-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac757-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac757-105">DESCRIPTION</span></span>
<span data-ttu-id="ac757-106">**Uruchomienie programu AzRecoveryServicesAsrApplyRecoveryPoint** powoduje zmianę punktu odzyskiwania dla elementu chronionego niepowodzeniem przed zatwierdzeniem operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="ac757-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="ac757-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac757-107">EXAMPLES</span></span>

### <span data-ttu-id="ac757-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac757-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="ac757-109">Rozpoczyna stosowanie określonego punktu odzyskiwania do elementu chronionego replikacji i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ac757-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ac757-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac757-110">PARAMETERS</span></span>

### <span data-ttu-id="ac757-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ac757-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ac757-112">Określa podstawowy plik certyfikatu, jeśli jest używane szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="ac757-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac757-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ac757-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ac757-114">Określa pomocniczy plik certyfikatu, jeśli jest używany szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="ac757-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac757-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac757-115">-DefaultProfile</span></span>
<span data-ttu-id="ac757-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac757-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac757-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ac757-117">-RecoveryPoint</span></span>
<span data-ttu-id="ac757-118">Określa obiekt punktu odzyskiwania odpowiadający punktowi odzyskiwania, który ma zostać zastosowany.</span><span class="sxs-lookup"><span data-stu-id="ac757-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac757-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ac757-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ac757-120">Określa obiekt elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="ac757-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac757-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac757-121">-Confirm</span></span>
<span data-ttu-id="ac757-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac757-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac757-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac757-123">-WhatIf</span></span>
<span data-ttu-id="ac757-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac757-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac757-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac757-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac757-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac757-126">CommonParameters</span></span>
<span data-ttu-id="ac757-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac757-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac757-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac757-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac757-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac757-129">INPUTS</span></span>

### <span data-ttu-id="ac757-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ac757-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ac757-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac757-131">OUTPUTS</span></span>

### <span data-ttu-id="ac757-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ac757-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ac757-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac757-133">NOTES</span></span>

## <span data-ttu-id="ac757-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac757-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac757-135">Polecenia cmdlet dotyczące odzyskiwania witryny Azure Site</span><span class="sxs-lookup"><span data-stu-id="ac757-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)

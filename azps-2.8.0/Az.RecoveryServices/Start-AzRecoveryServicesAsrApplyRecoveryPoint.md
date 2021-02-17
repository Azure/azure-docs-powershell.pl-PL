---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 6200ea42da8a15c96b8138acbd4a54ce7d88b101
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408665"
---
# <span data-ttu-id="9a26e-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a26e-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="9a26e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a26e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a26e-103">Zmienia punkt odzyskiwania dla elementu chronionego w trybie failover przed zatwierdzeniem operacji trybu failover.</span><span class="sxs-lookup"><span data-stu-id="9a26e-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="9a26e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a26e-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a26e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a26e-105">DESCRIPTION</span></span>
<span data-ttu-id="9a26e-106">Element **startowy AzRecoveryServicesAsrApplyRecoveryPoint** zmienia punkt odzyskiwania dla elementu, który został zabezpieczony niepowodzeniem, zanim zatwierdzi operację trybu failover.</span><span class="sxs-lookup"><span data-stu-id="9a26e-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="9a26e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a26e-107">EXAMPLES</span></span>

### <span data-ttu-id="9a26e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a26e-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="9a26e-109">Rozpoczyna stosowanie określonego punktu odzyskiwania do elementu chronionego replikacją i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9a26e-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9a26e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a26e-110">PARAMETERS</span></span>

### <span data-ttu-id="9a26e-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9a26e-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="9a26e-112">Określa plik certyfikatu podstawowego, jeśli jest używane szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="9a26e-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="9a26e-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9a26e-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="9a26e-114">Określa pomocniczy plik certyfikatu, jeśli jest używane szyfrowanie danych.</span><span class="sxs-lookup"><span data-stu-id="9a26e-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="9a26e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a26e-115">-DefaultProfile</span></span>
<span data-ttu-id="9a26e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a26e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9a26e-117">- RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a26e-117">-RecoveryPoint</span></span>
<span data-ttu-id="9a26e-118">Określa obiekt punktu odzyskiwania odpowiadający punktowi odzyskiwania, który ma zostać zastosowany.</span><span class="sxs-lookup"><span data-stu-id="9a26e-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="9a26e-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a26e-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9a26e-120">Określa obiekt elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="9a26e-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="9a26e-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a26e-121">-Confirm</span></span>
<span data-ttu-id="9a26e-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a26e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a26e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a26e-123">-WhatIf</span></span>
<span data-ttu-id="9a26e-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a26e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a26e-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a26e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a26e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a26e-126">CommonParameters</span></span>
<span data-ttu-id="9a26e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a26e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a26e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a26e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a26e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a26e-129">INPUTS</span></span>

### <span data-ttu-id="9a26e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a26e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9a26e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a26e-131">OUTPUTS</span></span>

### <span data-ttu-id="9a26e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9a26e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9a26e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a26e-133">NOTES</span></span>

## <span data-ttu-id="9a26e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a26e-134">RELATED LINKS</span></span>



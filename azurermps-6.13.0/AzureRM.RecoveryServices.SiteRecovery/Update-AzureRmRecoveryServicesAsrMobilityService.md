---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 539a0471ae27adc80b67360fc47955fdb4b50bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526113"
---
# <span data-ttu-id="155f9-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="155f9-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="155f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="155f9-102">SYNOPSIS</span></span>
<span data-ttu-id="155f9-103">Aktualizacje agenta usługi mobilności push na chronione komputery.</span><span class="sxs-lookup"><span data-stu-id="155f9-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="155f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="155f9-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="155f9-105">DESCRIPTION</span></span>
<span data-ttu-id="155f9-106">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrMobilityService** próbuje przepchnąć aktualizacje agenta usługi mobilności na chronione komputery (Jeśli aktualizacja jest dostępna).</span><span class="sxs-lookup"><span data-stu-id="155f9-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="155f9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="155f9-107">EXAMPLES</span></span>

### <span data-ttu-id="155f9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="155f9-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="155f9-109">Zadanie śledzenia agenta usługi Moblility chronionego elementu chronionego replikacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="155f9-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="155f9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="155f9-110">PARAMETERS</span></span>

### <span data-ttu-id="155f9-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="155f9-111">-Account</span></span>
<span data-ttu-id="155f9-112">Identyfikator konta Uruchom jako, który ma być używany do wypychania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="155f9-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="155f9-113">Musi znajdować się na liście kont Uruchom jako w sieci szkieletowej ASR odpowiadającej aktualizowanemu komputerowi.</span><span class="sxs-lookup"><span data-stu-id="155f9-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155f9-114">-DefaultProfile</span></span>
<span data-ttu-id="155f9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="155f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="155f9-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="155f9-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="155f9-117">Element chroniony replikacji odzyskiwania witryny Azure do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="155f9-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="155f9-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="155f9-118">-Confirm</span></span>
<span data-ttu-id="155f9-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155f9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="155f9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155f9-120">-WhatIf</span></span>
<span data-ttu-id="155f9-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155f9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="155f9-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="155f9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="155f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155f9-123">CommonParameters</span></span>
<span data-ttu-id="155f9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="155f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155f9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="155f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155f9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="155f9-126">INPUTS</span></span>

### <span data-ttu-id="155f9-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="155f9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="155f9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="155f9-128">OUTPUTS</span></span>

### <span data-ttu-id="155f9-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="155f9-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="155f9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="155f9-130">NOTES</span></span>

## <span data-ttu-id="155f9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="155f9-131">RELATED LINKS</span></span>

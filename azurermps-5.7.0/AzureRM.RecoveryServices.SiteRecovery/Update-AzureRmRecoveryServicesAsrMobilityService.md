---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: de9e07da334e252db4af87819d2719b5251b576c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524997"
---
# <span data-ttu-id="eb23f-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="eb23f-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="eb23f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb23f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb23f-103">Aktualizacje agenta usługi mobilności push na chronione komputery.</span><span class="sxs-lookup"><span data-stu-id="eb23f-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb23f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb23f-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb23f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb23f-105">DESCRIPTION</span></span>
<span data-ttu-id="eb23f-106">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrMobilityService** próbuje przepchnąć aktualizacje agenta usługi mobilności na chronione komputery (Jeśli aktualizacja jest dostępna).</span><span class="sxs-lookup"><span data-stu-id="eb23f-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="eb23f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb23f-107">EXAMPLES</span></span>

### <span data-ttu-id="eb23f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb23f-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="eb23f-109">Zadanie śledzenia agenta usługi Moblility chronionego elementu chronionego replikacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="eb23f-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="eb23f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb23f-110">PARAMETERS</span></span>

### <span data-ttu-id="eb23f-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="eb23f-111">-Account</span></span>
<span data-ttu-id="eb23f-112">Identyfikator konta Uruchom jako, który ma być używany do wypychania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="eb23f-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="eb23f-113">Musi znajdować się na liście kont Uruchom jako w sieci szkieletowej ASR odpowiadającej aktualizowanemu komputerowi.</span><span class="sxs-lookup"><span data-stu-id="eb23f-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb23f-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb23f-114">-Confirm</span></span>
<span data-ttu-id="eb23f-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb23f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb23f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb23f-116">-DefaultProfile</span></span>
<span data-ttu-id="eb23f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb23f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb23f-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eb23f-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="eb23f-119">Element chroniony replikacji odzyskiwania witryny Azure do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="eb23f-119">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="eb23f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb23f-120">-WhatIf</span></span>
<span data-ttu-id="eb23f-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb23f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb23f-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb23f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb23f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb23f-123">CommonParameters</span></span>
<span data-ttu-id="eb23f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb23f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb23f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb23f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb23f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb23f-126">INPUTS</span></span>

### <span data-ttu-id="eb23f-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="eb23f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="eb23f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb23f-128">OUTPUTS</span></span>

### <span data-ttu-id="eb23f-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eb23f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eb23f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb23f-130">NOTES</span></span>

## <span data-ttu-id="eb23f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb23f-131">RELATED LINKS</span></span>

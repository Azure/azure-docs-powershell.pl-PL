---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526129"
---
# <span data-ttu-id="a67c7-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a67c7-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="a67c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a67c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a67c7-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a67c7-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a67c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a67c7-104">SYNTAX</span></span>

### <span data-ttu-id="a67c7-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a67c7-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67c7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a67c7-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67c7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a67c7-107">DESCRIPTION</span></span>
<span data-ttu-id="a67c7-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="a67c7-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="a67c7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a67c7-109">EXAMPLES</span></span>

### <span data-ttu-id="a67c7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a67c7-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="a67c7-111">Rozpoczyna przechodzenie do trybu failover dla określonego planu odzyskiwania i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a67c7-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a67c7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a67c7-112">PARAMETERS</span></span>

### <span data-ttu-id="a67c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67c7-113">-DefaultProfile</span></span>
<span data-ttu-id="a67c7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a67c7-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a67c7-115">-RecoveryPlan</span></span>
<span data-ttu-id="a67c7-116">Określa obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania do przejęcia awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="a67c7-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a67c7-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a67c7-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a67c7-118">Określa obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej przed replikacją.</span><span class="sxs-lookup"><span data-stu-id="a67c7-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a67c7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a67c7-119">-Confirm</span></span>
<span data-ttu-id="a67c7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67c7-121">-WhatIf</span></span>
<span data-ttu-id="a67c7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67c7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a67c7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a67c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67c7-124">CommonParameters</span></span>
<span data-ttu-id="a67c7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67c7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a67c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67c7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67c7-127">INPUTS</span></span>

### <span data-ttu-id="a67c7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a67c7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="a67c7-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a67c7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a67c7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a67c7-130">OUTPUTS</span></span>

### <span data-ttu-id="a67c7-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a67c7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a67c7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a67c7-132">NOTES</span></span>

## <span data-ttu-id="a67c7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a67c7-133">RELATED LINKS</span></span>

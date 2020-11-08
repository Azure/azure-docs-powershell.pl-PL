---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 0714fc44ba8e52536e1a3eb677199da95895bc83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050581"
---
# <span data-ttu-id="a5e3b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a5e3b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="a5e3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e3b-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="a5e3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5e3b-104">SYNTAX</span></span>

### <span data-ttu-id="a5e3b-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5e3b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e3b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a5e3b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e3b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a5e3b-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e3b-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="a5e3b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5e3b-109">EXAMPLES</span></span>

### <span data-ttu-id="a5e3b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5e3b-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="a5e3b-111">Rozpoczyna przechodzenie do trybu failover dla określonego planu odzyskiwania i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a5e3b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5e3b-112">PARAMETERS</span></span>

### <span data-ttu-id="a5e3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e3b-113">-DefaultProfile</span></span>
<span data-ttu-id="a5e3b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a5e3b-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a5e3b-115">-RecoveryPlan</span></span>
<span data-ttu-id="a5e3b-116">Określa obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania do przejęcia awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="a5e3b-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a5e3b-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a5e3b-118">Określa obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej przed replikacją.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="a5e3b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5e3b-119">-Confirm</span></span>
<span data-ttu-id="a5e3b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e3b-121">-WhatIf</span></span>
<span data-ttu-id="a5e3b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5e3b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e3b-124">CommonParameters</span></span>
<span data-ttu-id="a5e3b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e3b-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e3b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e3b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5e3b-127">INPUTS</span></span>

### <span data-ttu-id="a5e3b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a5e3b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="a5e3b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a5e3b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a5e3b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5e3b-130">OUTPUTS</span></span>

### <span data-ttu-id="a5e3b-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a5e3b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a5e3b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5e3b-132">NOTES</span></span>

## <span data-ttu-id="a5e3b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5e3b-133">RELATED LINKS</span></span>

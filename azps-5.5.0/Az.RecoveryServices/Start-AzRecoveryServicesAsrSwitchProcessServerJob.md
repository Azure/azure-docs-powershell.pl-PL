---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192834"
---
# <span data-ttu-id="ada4a-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="ada4a-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="ada4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada4a-102">SYNOPSIS</span></span>
<span data-ttu-id="ada4a-103">Przełączanie replikacji z jednego serwera procesu na inny w celu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ada4a-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="ada4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ada4a-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada4a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ada4a-105">DESCRIPTION</span></span>
<span data-ttu-id="ada4a-106">Przełącznik **Start-AzRecoveryServicesAsrSwitchProcessServerJob** przełącza ruch danych replikacji dla określonych maszyn wirtualnych lub określonego serwera procesu do określonego docelowego serwera procesu.</span><span class="sxs-lookup"><span data-stu-id="ada4a-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="ada4a-107">Służy do równoważenia obciążenia lub przełączania replikacji między serwerami procesów.</span><span class="sxs-lookup"><span data-stu-id="ada4a-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="ada4a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ada4a-108">EXAMPLES</span></span>

### <span data-ttu-id="ada4a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ada4a-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="ada4a-110">Zadanie śledzenia przełączania serwera procesów dla wszystkich elementów chronionych replikacją z źródłowego do docelowego serwera procesów.</span><span class="sxs-lookup"><span data-stu-id="ada4a-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="ada4a-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ada4a-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="ada4a-112">Zadanie śledzenia przełączania serwera procesów dla przekazywanego elementu chronionego replikacją z źródłowego do docelowego serwera procesów.</span><span class="sxs-lookup"><span data-stu-id="ada4a-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="ada4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada4a-113">PARAMETERS</span></span>

### <span data-ttu-id="ada4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada4a-114">-DefaultProfile</span></span>
<span data-ttu-id="ada4a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ada4a-116">— Materiał</span><span class="sxs-lookup"><span data-stu-id="ada4a-116">-Fabric</span></span>
<span data-ttu-id="ada4a-117">Sieć szkielet odzyskiwania witryn odpowiadająca serwerowi konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ada4a-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4a-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ada4a-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ada4a-119">Lista elementów chronionych replikacją, których serwer przetwarzania ma zostać przełączony.</span><span class="sxs-lookup"><span data-stu-id="ada4a-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4a-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="ada4a-120">-SourceProcessServer</span></span>
<span data-ttu-id="ada4a-121">Serwer procesu, z którym można przełączać replikację.</span><span class="sxs-lookup"><span data-stu-id="ada4a-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4a-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="ada4a-122">-TargetProcessServer</span></span>
<span data-ttu-id="ada4a-123">Serwer procesu do przełączania replikacji.</span><span class="sxs-lookup"><span data-stu-id="ada4a-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada4a-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ada4a-124">-Confirm</span></span>
<span data-ttu-id="ada4a-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ada4a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada4a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada4a-126">-WhatIf</span></span>
<span data-ttu-id="ada4a-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada4a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada4a-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ada4a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada4a-129">CommonParameters</span></span>
<span data-ttu-id="ada4a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada4a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada4a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada4a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada4a-132">INPUTS</span></span>

### <span data-ttu-id="ada4a-133">Brak</span><span class="sxs-lookup"><span data-stu-id="ada4a-133">None</span></span>

## <span data-ttu-id="ada4a-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada4a-134">OUTPUTS</span></span>

### <span data-ttu-id="ada4a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ada4a-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ada4a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ada4a-136">NOTES</span></span>

## <span data-ttu-id="ada4a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada4a-137">RELATED LINKS</span></span>

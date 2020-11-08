---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225526"
---
# <span data-ttu-id="60c2d-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="60c2d-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="60c2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="60c2d-103">Przełączanie replikacji z jednego serwera przetwarzania do innego w celu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="60c2d-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="60c2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60c2d-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c2d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="60c2d-106">**AzRecoveryServicesAsrSwitchProcessServerJob Start —** przełącza ruch danych replikacji dla określonych maszyn wirtualnych lub określonego serwera Process Server na określony docelowy serwer przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="60c2d-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="60c2d-107">Służy do równoważenia obciążenia lub przełączenia replikacji między serwerami procesów.</span><span class="sxs-lookup"><span data-stu-id="60c2d-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="60c2d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60c2d-108">EXAMPLES</span></span>

### <span data-ttu-id="60c2d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60c2d-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="60c2d-110">Zadanie śledzenia serwera procesu przełączania dla wszystkich chronionych elementów replikacji z serwera źródłowego na docelowy proces.</span><span class="sxs-lookup"><span data-stu-id="60c2d-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="60c2d-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="60c2d-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="60c2d-112">Zadanie śledzenia serwera procesu przełączania dla przerzuconego chronionego elementu replikacji ze źródła do docelowego serwera przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="60c2d-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="60c2d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60c2d-113">PARAMETERS</span></span>

### <span data-ttu-id="60c2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c2d-114">-DefaultProfile</span></span>
<span data-ttu-id="60c2d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60c2d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c2d-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="60c2d-116">-Fabric</span></span>
<span data-ttu-id="60c2d-117">Sieć szkieletowa odzyskiwania witryny odpowiadająca serwerowi konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="60c2d-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="60c2d-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="60c2d-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="60c2d-119">Lista elementów chronionych replikacją, których serwer przetwarzania ma zostać przełączony.</span><span class="sxs-lookup"><span data-stu-id="60c2d-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="60c2d-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="60c2d-120">-SourceProcessServer</span></span>
<span data-ttu-id="60c2d-121">Serwer przetwarzania, z którego chcesz przełączyć replikację.</span><span class="sxs-lookup"><span data-stu-id="60c2d-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="60c2d-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="60c2d-122">-TargetProcessServer</span></span>
<span data-ttu-id="60c2d-123">Serwer przetwarzania, na którym ma zostać przełączona replikacja.</span><span class="sxs-lookup"><span data-stu-id="60c2d-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="60c2d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60c2d-124">-Confirm</span></span>
<span data-ttu-id="60c2d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c2d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c2d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c2d-126">-WhatIf</span></span>
<span data-ttu-id="60c2d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c2d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c2d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60c2d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c2d-129">CommonParameters</span></span>
<span data-ttu-id="60c2d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c2d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60c2d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c2d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60c2d-132">INPUTS</span></span>

### <span data-ttu-id="60c2d-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="60c2d-133">None</span></span>

## <span data-ttu-id="60c2d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60c2d-134">OUTPUTS</span></span>

### <span data-ttu-id="60c2d-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="60c2d-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60c2d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60c2d-136">NOTES</span></span>

## <span data-ttu-id="60c2d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60c2d-137">RELATED LINKS</span></span>

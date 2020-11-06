---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526633"
---
# <span data-ttu-id="3f7ce-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="3f7ce-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="3f7ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7ce-103">Przełączanie replikacji z jednego serwera przetwarzania do innego w celu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f7ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f7ce-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f7ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f7ce-105">DESCRIPTION</span></span>
<span data-ttu-id="3f7ce-106">**AzureRmRecoveryServicesAsrSwitchProcessServerJob Start —** przełącza ruch danych replikacji dla określonych maszyn wirtualnych lub określonego serwera Process Server na określony docelowy serwer przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="3f7ce-107">Służy do równoważenia obciążenia lub przełączenia replikacji między serwerami procesów.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="3f7ce-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f7ce-108">EXAMPLES</span></span>

### <span data-ttu-id="3f7ce-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f7ce-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="3f7ce-110">Zadanie śledzenia serwera procesu przełączania dla wszystkich chronionych elementów replikacji z serwera źródłowego na docelowy proces.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="3f7ce-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3f7ce-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="3f7ce-112">Zadanie śledzenia serwera procesu przełączania dla przerzuconego chronionego elementu replikacji ze źródła do docelowego serwera przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="3f7ce-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f7ce-113">PARAMETERS</span></span>

### <span data-ttu-id="3f7ce-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f7ce-114">-Confirm</span></span>
<span data-ttu-id="3f7ce-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7ce-116">-DefaultProfile</span></span>
<span data-ttu-id="3f7ce-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f7ce-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="3f7ce-118">-Fabric</span></span>
<span data-ttu-id="3f7ce-119">Sieć szkieletowa odzyskiwania witryny odpowiadająca serwerowi konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f7ce-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3f7ce-121">Lista elementów chronionych replikacją, których serwer przetwarzania ma zostać przełączony.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="3f7ce-122">-SourceProcessServer</span></span>
<span data-ttu-id="3f7ce-123">Serwer przetwarzania, z którego chcesz przełączyć replikację.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="3f7ce-124">-TargetProcessServer</span></span>
<span data-ttu-id="3f7ce-125">Serwer przetwarzania, na którym ma zostać przełączona replikacja.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f7ce-126">-WhatIf</span></span>
<span data-ttu-id="3f7ce-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f7ce-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f7ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7ce-129">CommonParameters</span></span>
<span data-ttu-id="3f7ce-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f7ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7ce-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f7ce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7ce-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f7ce-132">INPUTS</span></span>

### <span data-ttu-id="3f7ce-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f7ce-133">None</span></span>

## <span data-ttu-id="3f7ce-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f7ce-134">OUTPUTS</span></span>

### <span data-ttu-id="3f7ce-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f7ce-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f7ce-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f7ce-136">NOTES</span></span>

## <span data-ttu-id="3f7ce-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f7ce-137">RELATED LINKS</span></span>

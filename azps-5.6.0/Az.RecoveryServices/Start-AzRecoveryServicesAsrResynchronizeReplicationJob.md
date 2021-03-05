---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0675756b21c5af56ff3dc3fdff3b48d3bc9c999c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987575"
---
# <span data-ttu-id="decb5-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="decb5-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="decb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="decb5-102">SYNOPSIS</span></span>
<span data-ttu-id="decb5-103">Rozpoczyna ponowną synchronizację replikacji.</span><span class="sxs-lookup"><span data-stu-id="decb5-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="decb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="decb5-104">SYNTAX</span></span>

### <span data-ttu-id="decb5-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="decb5-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="decb5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="decb5-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decb5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="decb5-107">DESCRIPTION</span></span>
<span data-ttu-id="decb5-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** rozpoczyna ponowne synchronizowanie replikacji dla określonego chronionego elementu, jeśli chroniony element znajduje się w stanie wymaganej ponownej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="decb5-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="decb5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="decb5-109">EXAMPLES</span></span>

### <span data-ttu-id="decb5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="decb5-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="decb5-111">Uruchamia zadanie ponownej synchronizacji replikacji dla elementu chronionego replikacją przekazaną.</span><span class="sxs-lookup"><span data-stu-id="decb5-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="decb5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="decb5-112">PARAMETERS</span></span>

### <span data-ttu-id="decb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decb5-113">-DefaultProfile</span></span>
<span data-ttu-id="decb5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="decb5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="decb5-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="decb5-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="decb5-116">Element chroniony replikacją asr w celu ponownej synchronizacji replikacji.</span><span class="sxs-lookup"><span data-stu-id="decb5-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="decb5-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="decb5-117">-ResourceId</span></span>
<span data-ttu-id="decb5-118">Identyfikator zasobu elementu chronionego replikacją w celu ponownej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="decb5-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="decb5-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="decb5-119">-Confirm</span></span>
<span data-ttu-id="decb5-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="decb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decb5-121">-WhatIf</span></span>
<span data-ttu-id="decb5-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="decb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decb5-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="decb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decb5-124">CommonParameters</span></span>
<span data-ttu-id="decb5-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decb5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="decb5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decb5-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="decb5-127">INPUTS</span></span>

### <span data-ttu-id="decb5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="decb5-128">System.String</span></span>

### <span data-ttu-id="decb5-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="decb5-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="decb5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="decb5-130">OUTPUTS</span></span>

### <span data-ttu-id="decb5-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="decb5-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="decb5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="decb5-132">NOTES</span></span>

## <span data-ttu-id="decb5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="decb5-133">RELATED LINKS</span></span>

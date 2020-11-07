---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896118"
---
# <span data-ttu-id="08808-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="08808-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="08808-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08808-102">SYNOPSIS</span></span>
<span data-ttu-id="08808-103">Rozpoczyna ponowną synchronizację replikacji.</span><span class="sxs-lookup"><span data-stu-id="08808-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="08808-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08808-104">SYNTAX</span></span>

### <span data-ttu-id="08808-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="08808-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08808-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08808-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08808-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08808-107">DESCRIPTION</span></span>
<span data-ttu-id="08808-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** rozpoczyna ponowną synchronizację replikacji określonego elementu chronionego, jeśli jest to wymagany stan chronionej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="08808-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="08808-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08808-109">EXAMPLES</span></span>

### <span data-ttu-id="08808-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08808-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="08808-111">Rozpoczyna zadanie ponownego synchronizowania replikacji w przypadku przerzuconego chronionego elementu replikacji.</span><span class="sxs-lookup"><span data-stu-id="08808-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="08808-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08808-112">PARAMETERS</span></span>

### <span data-ttu-id="08808-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08808-113">-DefaultProfile</span></span>
<span data-ttu-id="08808-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08808-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08808-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="08808-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="08808-116">Chroniony element replikacji ASR, aby ponownie zsynchronizować replikację.</span><span class="sxs-lookup"><span data-stu-id="08808-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="08808-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08808-117">-ResourceId</span></span>
<span data-ttu-id="08808-118">Identyfikator zasobu chronionego elementu replikacji do ponownej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="08808-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="08808-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08808-119">-Confirm</span></span>
<span data-ttu-id="08808-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08808-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08808-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08808-121">-WhatIf</span></span>
<span data-ttu-id="08808-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08808-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08808-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08808-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08808-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08808-124">CommonParameters</span></span>
<span data-ttu-id="08808-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08808-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08808-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08808-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08808-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08808-127">INPUTS</span></span>

### <span data-ttu-id="08808-128">System. String</span><span class="sxs-lookup"><span data-stu-id="08808-128">System.String</span></span>

### <span data-ttu-id="08808-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="08808-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="08808-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08808-130">OUTPUTS</span></span>

### <span data-ttu-id="08808-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="08808-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="08808-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08808-132">NOTES</span></span>

## <span data-ttu-id="08808-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08808-133">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 48a17c0b2bd8c1d62de1b3ebd5eccc5171d65837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886593"
---
# <span data-ttu-id="cee48-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="cee48-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="cee48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cee48-102">SYNOPSIS</span></span>
<span data-ttu-id="cee48-103">Rozpoczyna ponowną synchronizację replikacji.</span><span class="sxs-lookup"><span data-stu-id="cee48-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="cee48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cee48-104">SYNTAX</span></span>

### <span data-ttu-id="cee48-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cee48-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee48-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cee48-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee48-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cee48-107">DESCRIPTION</span></span>
<span data-ttu-id="cee48-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** rozpoczyna ponowną synchronizację replikacji określonego elementu chronionego, jeśli jest to wymagany stan chronionej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cee48-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="cee48-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cee48-109">EXAMPLES</span></span>

### <span data-ttu-id="cee48-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cee48-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="cee48-111">Rozpoczyna zadanie ponownego synchronizowania replikacji w przypadku przerzuconego chronionego elementu replikacji.</span><span class="sxs-lookup"><span data-stu-id="cee48-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="cee48-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cee48-112">PARAMETERS</span></span>

### <span data-ttu-id="cee48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee48-113">-DefaultProfile</span></span>
<span data-ttu-id="cee48-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cee48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee48-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cee48-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cee48-116">Chroniony element replikacji ASR, aby ponownie zsynchronizować replikację.</span><span class="sxs-lookup"><span data-stu-id="cee48-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="cee48-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cee48-117">-ResourceId</span></span>
<span data-ttu-id="cee48-118">Identyfikator zasobu chronionego elementu replikacji do ponownej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cee48-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="cee48-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cee48-119">-Confirm</span></span>
<span data-ttu-id="cee48-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cee48-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee48-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee48-121">-WhatIf</span></span>
<span data-ttu-id="cee48-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cee48-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee48-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cee48-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee48-124">CommonParameters</span></span>
<span data-ttu-id="cee48-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee48-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee48-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee48-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cee48-127">INPUTS</span></span>

### <span data-ttu-id="cee48-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cee48-128">System.String</span></span>

### <span data-ttu-id="cee48-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cee48-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cee48-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cee48-130">OUTPUTS</span></span>

### <span data-ttu-id="cee48-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cee48-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cee48-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cee48-132">NOTES</span></span>

## <span data-ttu-id="cee48-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cee48-133">RELATED LINKS</span></span>

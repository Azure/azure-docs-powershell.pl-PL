---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526642"
---
# <span data-ttu-id="c7342-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="c7342-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="c7342-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7342-102">SYNOPSIS</span></span>
<span data-ttu-id="c7342-103">Rozpoczyna ponowną synchronizację replikacji.</span><span class="sxs-lookup"><span data-stu-id="c7342-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7342-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7342-104">SYNTAX</span></span>

### <span data-ttu-id="c7342-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c7342-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7342-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7342-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7342-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c7342-107">DESCRIPTION</span></span>
<span data-ttu-id="c7342-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** rozpoczyna ponowną synchronizację replikacji określonego elementu chronionego, jeśli jest to wymagany stan chronionej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c7342-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="c7342-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7342-109">EXAMPLES</span></span>

### <span data-ttu-id="c7342-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7342-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="c7342-111">Rozpoczyna zadanie ponownego synchronizowania replikacji w przypadku przerzuconego chronionego elementu replikacji.</span><span class="sxs-lookup"><span data-stu-id="c7342-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="c7342-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7342-112">PARAMETERS</span></span>

### <span data-ttu-id="c7342-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7342-113">-Confirm</span></span>
<span data-ttu-id="c7342-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7342-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7342-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7342-115">-DefaultProfile</span></span>
<span data-ttu-id="c7342-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7342-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7342-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7342-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c7342-118">Chroniony element replikacji ASR, aby ponownie zsynchronizować replikację.</span><span class="sxs-lookup"><span data-stu-id="c7342-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7342-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7342-119">-ResourceId</span></span>
<span data-ttu-id="c7342-120">Identyfikator zasobu chronionego elementu replikacji do ponownej synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c7342-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7342-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7342-121">-WhatIf</span></span>
<span data-ttu-id="c7342-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7342-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7342-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7342-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7342-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7342-124">CommonParameters</span></span>
<span data-ttu-id="c7342-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7342-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7342-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7342-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7342-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7342-127">INPUTS</span></span>

### <span data-ttu-id="c7342-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c7342-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c7342-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7342-129">OUTPUTS</span></span>

### <span data-ttu-id="c7342-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c7342-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c7342-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7342-131">NOTES</span></span>

## <span data-ttu-id="c7342-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7342-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542887"
---
# <span data-ttu-id="9cf9c-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9cf9c-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="9cf9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cf9c-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf9c-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cf9c-104">SYNTAX</span></span>

### <span data-ttu-id="9cf9c-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9cf9c-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cf9c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9cf9c-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cf9c-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="9cf9c-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cf9c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9cf9c-108">DESCRIPTION</span></span>
<span data-ttu-id="9cf9c-109">Polecenie cmdlet **Start-AzureRmSiteRecoveryCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="9cf9c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cf9c-110">EXAMPLES</span></span>

## <span data-ttu-id="9cf9c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cf9c-111">PARAMETERS</span></span>

### <span data-ttu-id="9cf9c-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9cf9c-112">-ProtectionEntity</span></span>
<span data-ttu-id="9cf9c-113">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf9c-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cf9c-114">-RecoveryPlan</span></span>
<span data-ttu-id="9cf9c-115">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf9c-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9cf9c-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf9c-117">-DefaultProfile</span></span>
<span data-ttu-id="9cf9c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf9c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf9c-119">CommonParameters</span></span>
<span data-ttu-id="9cf9c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf9c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf9c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf9c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf9c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cf9c-122">INPUTS</span></span>

### <span data-ttu-id="9cf9c-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9cf9c-123">ASRProtectionEntity</span></span>
<span data-ttu-id="9cf9c-124">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9cf9c-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="9cf9c-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9cf9c-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="9cf9c-126">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9cf9c-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="9cf9c-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9cf9c-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="9cf9c-128">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9cf9c-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="9cf9c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cf9c-129">OUTPUTS</span></span>

### <span data-ttu-id="9cf9c-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9cf9c-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9cf9c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cf9c-131">NOTES</span></span>

## <span data-ttu-id="9cf9c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cf9c-132">RELATED LINKS</span></span>


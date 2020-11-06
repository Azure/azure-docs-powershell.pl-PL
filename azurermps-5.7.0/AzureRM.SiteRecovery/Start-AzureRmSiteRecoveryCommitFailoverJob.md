---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverycommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 839855b9b56e4ecc73552af310af7221c9b7b2d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551496"
---
# <span data-ttu-id="e4345-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e4345-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="e4345-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4345-102">SYNOPSIS</span></span>
<span data-ttu-id="e4345-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="e4345-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4345-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4345-104">SYNTAX</span></span>

### <span data-ttu-id="e4345-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4345-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4345-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e4345-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4345-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e4345-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4345-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4345-108">DESCRIPTION</span></span>
<span data-ttu-id="e4345-109">Polecenie cmdlet **Start-AzureRmSiteRecoveryCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="e4345-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="e4345-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4345-110">EXAMPLES</span></span>

## <span data-ttu-id="e4345-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4345-111">PARAMETERS</span></span>

### <span data-ttu-id="e4345-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4345-112">-DefaultProfile</span></span>
<span data-ttu-id="e4345-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4345-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4345-114">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e4345-114">-ProtectionEntity</span></span>
<span data-ttu-id="e4345-115">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="e4345-115">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4345-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e4345-116">-RecoveryPlan</span></span>
<span data-ttu-id="e4345-117">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e4345-117">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4345-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4345-118">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4345-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4345-119">CommonParameters</span></span>
<span data-ttu-id="e4345-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4345-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4345-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4345-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4345-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4345-122">INPUTS</span></span>

### <span data-ttu-id="e4345-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e4345-123">ASRProtectionEntity</span></span>
<span data-ttu-id="e4345-124">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e4345-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="e4345-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e4345-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="e4345-126">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e4345-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="e4345-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e4345-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="e4345-128">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e4345-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="e4345-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4345-129">OUTPUTS</span></span>

### <span data-ttu-id="e4345-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e4345-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e4345-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4345-131">NOTES</span></span>

## <span data-ttu-id="e4345-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4345-132">RELATED LINKS</span></span>


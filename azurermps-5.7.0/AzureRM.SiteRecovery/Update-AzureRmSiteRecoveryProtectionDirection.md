---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: f7d8efcde5f60ed9cf6eb3aff7f86c9ea3171ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524886"
---
# <span data-ttu-id="3e96e-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="3e96e-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="3e96e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e96e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e96e-103">Umożliwia zaktualizowanie serwera źródłowego i docelowego w celu ochrony obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="3e96e-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e96e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e96e-104">SYNTAX</span></span>

### <span data-ttu-id="3e96e-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e96e-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e96e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3e96e-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e96e-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="3e96e-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e96e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e96e-108">DESCRIPTION</span></span>
<span data-ttu-id="3e96e-109">Polecenie cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aktualizuje serwer źródłowy i docelowy w celu ochrony obiektu odzyskiwania witryny Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3e96e-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="3e96e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e96e-110">EXAMPLES</span></span>

## <span data-ttu-id="3e96e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e96e-111">PARAMETERS</span></span>

### <span data-ttu-id="3e96e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e96e-112">-DefaultProfile</span></span>
<span data-ttu-id="3e96e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e96e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e96e-114">-Direction</span><span class="sxs-lookup"><span data-stu-id="3e96e-114">-Direction</span></span>
<span data-ttu-id="3e96e-115">Określa kierunek zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="3e96e-115">Specifies the direction of the commit.</span></span>
<span data-ttu-id="3e96e-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3e96e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e96e-117">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3e96e-117">PrimaryToRecovery</span></span>
- <span data-ttu-id="3e96e-118">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3e96e-118">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e96e-119">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e96e-119">-ProtectionEntity</span></span>
<span data-ttu-id="3e96e-120">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="3e96e-120">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="3e96e-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3e96e-121">-RecoveryPlan</span></span>
<span data-ttu-id="3e96e-122">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3e96e-122">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="3e96e-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e96e-123">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="3e96e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e96e-124">CommonParameters</span></span>
<span data-ttu-id="3e96e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e96e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e96e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e96e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e96e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e96e-127">INPUTS</span></span>

### <span data-ttu-id="3e96e-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e96e-128">ASRProtectionEntity</span></span>
<span data-ttu-id="3e96e-129">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3e96e-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="3e96e-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3e96e-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="3e96e-131">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3e96e-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="3e96e-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e96e-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="3e96e-133">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3e96e-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="3e96e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e96e-134">OUTPUTS</span></span>

### <span data-ttu-id="3e96e-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3e96e-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3e96e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e96e-136">NOTES</span></span>

## <span data-ttu-id="3e96e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e96e-137">RELATED LINKS</span></span>


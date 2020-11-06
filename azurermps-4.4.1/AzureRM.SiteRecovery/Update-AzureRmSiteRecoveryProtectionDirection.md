---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542867"
---
# <span data-ttu-id="dd66e-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="dd66e-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="dd66e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd66e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd66e-103">Umożliwia zaktualizowanie serwera źródłowego i docelowego w celu ochrony obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="dd66e-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd66e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd66e-104">SYNTAX</span></span>

### <span data-ttu-id="dd66e-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd66e-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd66e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="dd66e-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd66e-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="dd66e-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd66e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dd66e-108">DESCRIPTION</span></span>
<span data-ttu-id="dd66e-109">Polecenie cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aktualizuje serwer źródłowy i docelowy w celu ochrony obiektu odzyskiwania witryny Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="dd66e-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="dd66e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd66e-110">EXAMPLES</span></span>

## <span data-ttu-id="dd66e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd66e-111">PARAMETERS</span></span>

### <span data-ttu-id="dd66e-112">-Direction</span><span class="sxs-lookup"><span data-stu-id="dd66e-112">-Direction</span></span>
<span data-ttu-id="dd66e-113">Określa kierunek zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="dd66e-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="dd66e-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dd66e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd66e-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="dd66e-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="dd66e-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="dd66e-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd66e-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dd66e-117">-ProtectionEntity</span></span>
<span data-ttu-id="dd66e-118">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="dd66e-118">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="dd66e-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dd66e-119">-RecoveryPlan</span></span>
<span data-ttu-id="dd66e-120">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="dd66e-120">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="dd66e-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dd66e-121">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="dd66e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd66e-122">-DefaultProfile</span></span>
<span data-ttu-id="dd66e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd66e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd66e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd66e-124">CommonParameters</span></span>
<span data-ttu-id="dd66e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd66e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd66e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd66e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd66e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd66e-127">INPUTS</span></span>

### <span data-ttu-id="dd66e-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dd66e-128">ASRProtectionEntity</span></span>
<span data-ttu-id="dd66e-129">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd66e-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="dd66e-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dd66e-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="dd66e-131">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd66e-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="dd66e-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dd66e-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="dd66e-133">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd66e-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="dd66e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd66e-134">OUTPUTS</span></span>

### <span data-ttu-id="dd66e-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dd66e-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dd66e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd66e-136">NOTES</span></span>

## <span data-ttu-id="dd66e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd66e-137">RELATED LINKS</span></span>


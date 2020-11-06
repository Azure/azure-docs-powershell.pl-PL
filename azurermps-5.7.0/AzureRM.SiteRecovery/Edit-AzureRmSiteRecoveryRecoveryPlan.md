---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550536"
---
# <span data-ttu-id="b3732-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b3732-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="b3732-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3732-102">SYNOPSIS</span></span>
<span data-ttu-id="b3732-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b3732-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3732-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3732-104">SYNTAX</span></span>

### <span data-ttu-id="b3732-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b3732-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3732-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="b3732-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3732-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="b3732-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3732-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="b3732-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3732-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="b3732-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3732-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="b3732-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3732-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b3732-111">DESCRIPTION</span></span>
<span data-ttu-id="b3732-112">Polecenie cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3732-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="b3732-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3732-113">EXAMPLES</span></span>

## <span data-ttu-id="b3732-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3732-114">PARAMETERS</span></span>

### <span data-ttu-id="b3732-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="b3732-115">-AddProtectedEntities</span></span>
<span data-ttu-id="b3732-116">Określa tablicę chronionych encji, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="b3732-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="b3732-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-118">-Append</span><span class="sxs-lookup"><span data-stu-id="b3732-118">-AppendGroup</span></span>
<span data-ttu-id="b3732-119">Wskazuje, że ta operacja dołącza grupę do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b3732-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3732-120">-DefaultProfile</span></span>
<span data-ttu-id="b3732-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3732-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3732-122">-Group</span><span class="sxs-lookup"><span data-stu-id="b3732-122">-Group</span></span>
<span data-ttu-id="b3732-123">Określa grupę planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b3732-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b3732-124">-RecoveryPlan</span></span>
<span data-ttu-id="b3732-125">Określa plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b3732-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-126">-Remove</span><span class="sxs-lookup"><span data-stu-id="b3732-126">-RemoveGroup</span></span>
<span data-ttu-id="b3732-127">Usuwa określoną grupę planów odzyskiwania dla odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b3732-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="b3732-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="b3732-129">Określa tablicę chronionych jednostek.</span><span class="sxs-lookup"><span data-stu-id="b3732-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="b3732-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3732-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3732-131">CommonParameters</span></span>
<span data-ttu-id="b3732-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3732-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3732-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3732-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3732-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3732-134">INPUTS</span></span>

### <span data-ttu-id="b3732-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b3732-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="b3732-136">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b3732-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="b3732-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3732-137">OUTPUTS</span></span>

## <span data-ttu-id="b3732-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3732-138">NOTES</span></span>

## <span data-ttu-id="b3732-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3732-139">RELATED LINKS</span></span>

[<span data-ttu-id="b3732-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b3732-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b3732-141">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b3732-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

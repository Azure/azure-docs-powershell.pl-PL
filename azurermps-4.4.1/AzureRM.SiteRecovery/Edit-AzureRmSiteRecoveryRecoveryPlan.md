---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716873"
---
# <span data-ttu-id="2ab73-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ab73-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="2ab73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ab73-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab73-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2ab73-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ab73-104">SYNTAX</span></span>

### <span data-ttu-id="2ab73-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2ab73-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab73-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="2ab73-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab73-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="2ab73-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab73-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="2ab73-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab73-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2ab73-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab73-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2ab73-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab73-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2ab73-111">DESCRIPTION</span></span>
<span data-ttu-id="2ab73-112">Polecenie cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab73-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="2ab73-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ab73-113">EXAMPLES</span></span>

## <span data-ttu-id="2ab73-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ab73-114">PARAMETERS</span></span>

### <span data-ttu-id="2ab73-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="2ab73-115">-AddProtectedEntities</span></span>
<span data-ttu-id="2ab73-116">Określa tablicę chronionych encji, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="2ab73-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2ab73-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-118">-Append</span><span class="sxs-lookup"><span data-stu-id="2ab73-118">-AppendGroup</span></span>
<span data-ttu-id="2ab73-119">Wskazuje, że ta operacja dołącza grupę do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="2ab73-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-120">-Group</span><span class="sxs-lookup"><span data-stu-id="2ab73-120">-Group</span></span>
<span data-ttu-id="2ab73-121">Określa grupę planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2ab73-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ab73-122">-RecoveryPlan</span></span>
<span data-ttu-id="2ab73-123">Określa plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="2ab73-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-124">-Remove</span><span class="sxs-lookup"><span data-stu-id="2ab73-124">-RemoveGroup</span></span>
<span data-ttu-id="2ab73-125">Usuwa określoną grupę planów odzyskiwania dla odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2ab73-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="2ab73-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="2ab73-127">Określa tablicę chronionych jednostek.</span><span class="sxs-lookup"><span data-stu-id="2ab73-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="2ab73-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab73-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab73-129">-DefaultProfile</span></span>
<span data-ttu-id="2ab73-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab73-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ab73-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab73-131">CommonParameters</span></span>
<span data-ttu-id="2ab73-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab73-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab73-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab73-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab73-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ab73-134">INPUTS</span></span>

### <span data-ttu-id="2ab73-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ab73-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="2ab73-136">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2ab73-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="2ab73-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ab73-137">OUTPUTS</span></span>

## <span data-ttu-id="2ab73-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ab73-138">NOTES</span></span>

## <span data-ttu-id="2ab73-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ab73-139">RELATED LINKS</span></span>

[<span data-ttu-id="2ab73-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ab73-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2ab73-141">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ab73-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

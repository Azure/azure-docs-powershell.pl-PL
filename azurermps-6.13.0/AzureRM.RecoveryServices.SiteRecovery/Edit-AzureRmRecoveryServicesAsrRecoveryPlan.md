---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548604"
---
# <span data-ttu-id="a364d-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a364d-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a364d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a364d-102">SYNOPSIS</span></span>
<span data-ttu-id="a364d-103">Umożliwia edytowanie planu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a364d-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a364d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a364d-104">SYNTAX</span></span>

### <span data-ttu-id="a364d-105">Append (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a364d-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a364d-106">Usuń</span><span class="sxs-lookup"><span data-stu-id="a364d-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a364d-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="a364d-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a364d-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="a364d-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a364d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a364d-109">DESCRIPTION</span></span>
<span data-ttu-id="a364d-110">Polecenie cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** edytuje plan odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a364d-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="a364d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a364d-111">EXAMPLES</span></span>

### <span data-ttu-id="a364d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a364d-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="a364d-113">Dołącza grupę do istniejącego planu odzyskiwania usługi Azure Site Recovery i zwraca zaktualizowany plan odzyskiwania w pamięci.</span><span class="sxs-lookup"><span data-stu-id="a364d-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="a364d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a364d-114">PARAMETERS</span></span>

### <span data-ttu-id="a364d-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a364d-115">-AddProtectedItem</span></span>
<span data-ttu-id="a364d-116">Lista elementów chronionych replikacji ASR, które mają zostać dodane do grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a364d-117">-Append</span><span class="sxs-lookup"><span data-stu-id="a364d-117">-AppendGroup</span></span>
<span data-ttu-id="a364d-118">Parametr Przełącz umożliwiający dołączenie grupy planu odzyskiwania do obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="a364d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a364d-119">-DefaultProfile</span></span>
<span data-ttu-id="a364d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a364d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a364d-121">-Group</span><span class="sxs-lookup"><span data-stu-id="a364d-121">-Group</span></span>
<span data-ttu-id="a364d-122">Określa grupę planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a364d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a364d-123">-InputObject</span></span>
<span data-ttu-id="a364d-124">Obiekt planu odzyskiwania ASR, który ma być edytowany (w ramach operacji pamięci.</span><span class="sxs-lookup"><span data-stu-id="a364d-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="a364d-125">Aby zaktualizować plan odzyskiwania Update-AzureRmASRRecoveryPlan Uruchom obiekt z edytowanym planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a364d-126">-Remove</span><span class="sxs-lookup"><span data-stu-id="a364d-126">-RemoveGroup</span></span>
<span data-ttu-id="a364d-127">Usuwa określoną grupę z obiektu planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a364d-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a364d-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="a364d-129">Lista elementów chronionych replikacji ASR do usunięcia z grupy plan odzyskiwania w obiekcie plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a364d-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a364d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a364d-130">-Confirm</span></span>
<span data-ttu-id="a364d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a364d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a364d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a364d-132">-WhatIf</span></span>
<span data-ttu-id="a364d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a364d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a364d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a364d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a364d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a364d-135">CommonParameters</span></span>
<span data-ttu-id="a364d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a364d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a364d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a364d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a364d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a364d-138">INPUTS</span></span>

### <span data-ttu-id="a364d-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a364d-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a364d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a364d-140">OUTPUTS</span></span>

### <span data-ttu-id="a364d-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="a364d-141">System.Object</span></span>

## <span data-ttu-id="a364d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a364d-142">NOTES</span></span>

## <span data-ttu-id="a364d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a364d-143">RELATED LINKS</span></span>

[<span data-ttu-id="a364d-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a364d-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a364d-145">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a364d-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719260"
---
# <span data-ttu-id="221ae-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="221ae-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="221ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="221ae-102">SYNOPSIS</span></span>
<span data-ttu-id="221ae-103">Umożliwia odzyskanie określonego planu odzyskiwania ASR z magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="221ae-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="221ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="221ae-104">SYNTAX</span></span>

### <span data-ttu-id="221ae-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="221ae-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="221ae-106">ByName</span><span class="sxs-lookup"><span data-stu-id="221ae-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="221ae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="221ae-107">DESCRIPTION</span></span>
<span data-ttu-id="221ae-108">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** usuwa określony plan odzyskiwania z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="221ae-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="221ae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="221ae-109">EXAMPLES</span></span>

### <span data-ttu-id="221ae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="221ae-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="221ae-111">Rozpoczyna usuwanie określonego planu odzyskiwania i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="221ae-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="221ae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="221ae-112">PARAMETERS</span></span>

### <span data-ttu-id="221ae-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="221ae-113">-InputObject</span></span>
<span data-ttu-id="221ae-114">Obiekt wejściowy do polecenia cmdlet: obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="221ae-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="221ae-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="221ae-115">-Name</span></span>
<span data-ttu-id="221ae-116">Określa nazwę planu odzyskiwania, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="221ae-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="221ae-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="221ae-117">-Confirm</span></span>
<span data-ttu-id="221ae-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="221ae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="221ae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="221ae-119">-WhatIf</span></span>
<span data-ttu-id="221ae-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="221ae-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="221ae-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="221ae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="221ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221ae-122">CommonParameters</span></span>
<span data-ttu-id="221ae-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="221ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221ae-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="221ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221ae-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="221ae-125">INPUTS</span></span>

### <span data-ttu-id="221ae-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="221ae-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="221ae-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="221ae-127">OUTPUTS</span></span>

### <span data-ttu-id="221ae-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="221ae-128">System.Object</span></span>

## <span data-ttu-id="221ae-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="221ae-129">NOTES</span></span>

## <span data-ttu-id="221ae-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="221ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="221ae-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="221ae-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="221ae-132">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="221ae-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="221ae-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="221ae-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)



---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718113"
---
# <span data-ttu-id="b2944-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2944-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b2944-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2944-102">SYNOPSIS</span></span>
<span data-ttu-id="b2944-103">Aktualizuje zawartość planu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b2944-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2944-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2944-104">SYNTAX</span></span>

### <span data-ttu-id="b2944-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2944-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2944-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b2944-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2944-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b2944-107">DESCRIPTION</span></span>
<span data-ttu-id="b2944-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** aktualizuje zawartość planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania ASR lub pliku JSON definicji planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="b2944-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="b2944-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2944-109">EXAMPLES</span></span>

### <span data-ttu-id="b2944-110">Przykład 1: aktualizowanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="b2944-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="b2944-111">Rozpoczynanie operacji aktualizowania planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b2944-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b2944-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2944-112">PARAMETERS</span></span>

### <span data-ttu-id="b2944-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2944-113">-InputObject</span></span>
<span data-ttu-id="b2944-114">Obiekt wejściowy do polecenia cmdlet: określa obiekt planu odzyskiwania ASR, którego zawartość jest używana do aktualizowania planu odzyskiwania, do którego odwołuje się obiekt.</span><span class="sxs-lookup"><span data-stu-id="b2944-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2944-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b2944-115">-Path</span></span>
<span data-ttu-id="b2944-116">Określa ścieżkę pliku JSON definicji planu odzyskiwania służącego do aktualizowania planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b2944-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2944-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2944-117">-Confirm</span></span>
<span data-ttu-id="b2944-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2944-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2944-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2944-119">-WhatIf</span></span>
<span data-ttu-id="b2944-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2944-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2944-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2944-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2944-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2944-122">CommonParameters</span></span>
<span data-ttu-id="b2944-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2944-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2944-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2944-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2944-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2944-125">INPUTS</span></span>

### <span data-ttu-id="b2944-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2944-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="b2944-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2944-127">OUTPUTS</span></span>

### <span data-ttu-id="b2944-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="b2944-128">System.Object</span></span>

## <span data-ttu-id="b2944-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2944-129">NOTES</span></span>

## <span data-ttu-id="b2944-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2944-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2944-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2944-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2944-132">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2944-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2944-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2944-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)



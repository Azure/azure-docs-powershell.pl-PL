---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: eb42cdf74482a5161ab75df459c78d88749fde7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544899"
---
# <span data-ttu-id="f4ddc-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4ddc-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f4ddc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ddc-103">Aktualizuje zawartość planu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4ddc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4ddc-104">SYNTAX</span></span>

### <span data-ttu-id="f4ddc-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4ddc-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ddc-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="f4ddc-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ddc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4ddc-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ddc-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** aktualizuje zawartość planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania ASR lub pliku JSON definicji planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="f4ddc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4ddc-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ddc-110">Przykład 1: aktualizowanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="f4ddc-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f4ddc-111">Rozpoczynanie operacji aktualizowania planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f4ddc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4ddc-112">PARAMETERS</span></span>

### <span data-ttu-id="f4ddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ddc-113">-DefaultProfile</span></span>
<span data-ttu-id="f4ddc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f4ddc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4ddc-115">-InputObject</span></span>
<span data-ttu-id="f4ddc-116">Obiekt wejściowy do polecenia cmdlet: określa obiekt planu odzyskiwania ASR, którego zawartość jest używana do aktualizowania planu odzyskiwania, do którego odwołuje się obiekt.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ddc-117">-Path</span><span class="sxs-lookup"><span data-stu-id="f4ddc-117">-Path</span></span>
<span data-ttu-id="f4ddc-118">Określa ścieżkę pliku JSON definicji planu odzyskiwania służącego do aktualizowania planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ddc-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4ddc-119">-Confirm</span></span>
<span data-ttu-id="f4ddc-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ddc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ddc-121">-WhatIf</span></span>
<span data-ttu-id="f4ddc-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4ddc-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ddc-124">CommonParameters</span></span>
<span data-ttu-id="f4ddc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ddc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ddc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ddc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ddc-127">INPUTS</span></span>

### <span data-ttu-id="f4ddc-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4ddc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f4ddc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4ddc-129">OUTPUTS</span></span>

### <span data-ttu-id="f4ddc-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f4ddc-130">System.Object</span></span>

## <span data-ttu-id="f4ddc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4ddc-131">NOTES</span></span>

## <span data-ttu-id="f4ddc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4ddc-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4ddc-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4ddc-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f4ddc-134">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4ddc-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f4ddc-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4ddc-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
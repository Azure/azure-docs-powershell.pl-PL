---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543064"
---
# <span data-ttu-id="cae8c-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cae8c-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="cae8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cae8c-102">SYNOPSIS</span></span>
<span data-ttu-id="cae8c-103">Usuwa określone zasady replikacji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cae8c-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cae8c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cae8c-105">DESCRIPTION</span></span>
<span data-ttu-id="cae8c-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrPolicy** usunęło określone zasady replikacji z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="cae8c-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="cae8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cae8c-107">EXAMPLES</span></span>

### <span data-ttu-id="cae8c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cae8c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="cae8c-109">Rozpoczyna usuwanie określonych zasad replikacji i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="cae8c-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cae8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cae8c-110">PARAMETERS</span></span>

### <span data-ttu-id="cae8c-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cae8c-111">-InputObject</span></span>
<span data-ttu-id="cae8c-112">Obiekt wejściowy do polecenia cmdlet: obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="cae8c-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae8c-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cae8c-113">-Confirm</span></span>
<span data-ttu-id="cae8c-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae8c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae8c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae8c-115">-WhatIf</span></span>
<span data-ttu-id="cae8c-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae8c-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cae8c-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cae8c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae8c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae8c-118">CommonParameters</span></span>
<span data-ttu-id="cae8c-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae8c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae8c-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae8c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae8c-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cae8c-121">INPUTS</span></span>

### <span data-ttu-id="cae8c-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="cae8c-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="cae8c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cae8c-123">OUTPUTS</span></span>

### <span data-ttu-id="cae8c-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="cae8c-124">System.Object</span></span>

## <span data-ttu-id="cae8c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cae8c-125">NOTES</span></span>

## <span data-ttu-id="cae8c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cae8c-126">RELATED LINKS</span></span>

[<span data-ttu-id="cae8c-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cae8c-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="cae8c-128">Nowe — AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cae8c-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

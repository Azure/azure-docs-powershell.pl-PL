---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543063"
---
# <span data-ttu-id="51d2f-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51d2f-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="51d2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="51d2f-103">Usuwa określone mapowanie sieci funkcji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="51d2f-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51d2f-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51d2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="51d2f-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** umożliwia usunięcie określonego mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="51d2f-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="51d2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51d2f-107">EXAMPLES</span></span>

### <span data-ttu-id="51d2f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51d2f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="51d2f-109">Rozpoczyna usuwanie określonego mapowania sieci funkcji ASR i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="51d2f-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="51d2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51d2f-110">PARAMETERS</span></span>

### <span data-ttu-id="51d2f-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51d2f-111">-InputObject</span></span>
<span data-ttu-id="51d2f-112">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="51d2f-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d2f-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51d2f-113">-Confirm</span></span>
<span data-ttu-id="51d2f-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51d2f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d2f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d2f-115">-WhatIf</span></span>
<span data-ttu-id="51d2f-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51d2f-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51d2f-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51d2f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d2f-118">CommonParameters</span></span>
<span data-ttu-id="51d2f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51d2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d2f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d2f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d2f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51d2f-121">INPUTS</span></span>

### <span data-ttu-id="51d2f-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51d2f-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="51d2f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51d2f-123">OUTPUTS</span></span>

### <span data-ttu-id="51d2f-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51d2f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51d2f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51d2f-125">NOTES</span></span>

## <span data-ttu-id="51d2f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51d2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="51d2f-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51d2f-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="51d2f-128">Nowe — AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51d2f-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

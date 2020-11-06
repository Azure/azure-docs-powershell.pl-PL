---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550832"
---
# <span data-ttu-id="07c54-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07c54-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="07c54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07c54-102">SYNOPSIS</span></span>
<span data-ttu-id="07c54-103">Usuwa określone mapowanie klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="07c54-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07c54-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07c54-105">DESCRIPTION</span></span>
<span data-ttu-id="07c54-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** usuwa określone mapowanie klasyfikacji magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="07c54-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="07c54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07c54-107">EXAMPLES</span></span>

### <span data-ttu-id="07c54-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07c54-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="07c54-109">Rozpoczyna usuwanie określonego mapowania klasyfikacji magazynu i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="07c54-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="07c54-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07c54-110">PARAMETERS</span></span>

### <span data-ttu-id="07c54-111">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="07c54-111">-InputObject</span></span>
<span data-ttu-id="07c54-112">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania klasyfikacji magazynu ASR odpowiadający mapowaniu klasyfikacji magazynu ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="07c54-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07c54-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07c54-113">-Confirm</span></span>
<span data-ttu-id="07c54-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c54-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c54-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c54-115">-WhatIf</span></span>
<span data-ttu-id="07c54-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c54-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07c54-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07c54-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c54-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c54-118">CommonParameters</span></span>
<span data-ttu-id="07c54-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c54-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c54-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c54-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c54-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07c54-121">INPUTS</span></span>

### <span data-ttu-id="07c54-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07c54-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="07c54-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07c54-123">OUTPUTS</span></span>

### <span data-ttu-id="07c54-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07c54-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07c54-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07c54-125">NOTES</span></span>

## <span data-ttu-id="07c54-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07c54-126">RELATED LINKS</span></span>

[<span data-ttu-id="07c54-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07c54-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="07c54-128">Nowe — AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07c54-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

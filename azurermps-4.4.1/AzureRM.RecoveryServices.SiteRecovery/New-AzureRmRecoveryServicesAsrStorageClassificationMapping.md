---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 14cd1606bc4c8d1709b0ddd64e845a2e84b26df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543071"
---
# <span data-ttu-id="ffb4c-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ffb4c-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ffb4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb4c-103">Tworzy mapowanie klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffb4c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb4c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb4c-106">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu na magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="ffb4c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb4c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffb4c-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="ffb4c-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ffb4c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffb4c-110">PARAMETERS</span></span>

### <span data-ttu-id="ffb4c-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ffb4c-111">-Name</span></span>
<span data-ttu-id="ffb4c-112">Określa nazwę mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-112">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb4c-113">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ffb4c-113">-PrimaryStorageClassification</span></span>
<span data-ttu-id="ffb4c-114">Określa podstawowy obiekt klasyfikacji magazynu ASR dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-114">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb4c-115">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ffb4c-115">-RecoveryStorageClassification</span></span>
<span data-ttu-id="ffb4c-116">Określa obiekt klasyfikacji magazynu ASR odzyskiwania w celu mapowania.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-116">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb4c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffb4c-117">-Confirm</span></span>
<span data-ttu-id="ffb4c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb4c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb4c-119">-WhatIf</span></span>
<span data-ttu-id="ffb4c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffb4c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb4c-122">CommonParameters</span></span>
<span data-ttu-id="ffb4c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb4c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb4c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb4c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffb4c-125">INPUTS</span></span>

### <span data-ttu-id="ffb4c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ffb4c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="ffb4c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffb4c-127">OUTPUTS</span></span>

### <span data-ttu-id="ffb4c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ffb4c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ffb4c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffb4c-129">NOTES</span></span>

## <span data-ttu-id="ffb4c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffb4c-130">RELATED LINKS</span></span>

[<span data-ttu-id="ffb4c-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ffb4c-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ffb4c-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ffb4c-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

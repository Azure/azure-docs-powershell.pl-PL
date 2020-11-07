---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718129"
---
# <span data-ttu-id="fd5ed-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd5ed-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="fd5ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5ed-103">Pobiera mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd5ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd5ed-104">SYNTAX</span></span>

### <span data-ttu-id="fd5ed-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd5ed-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="fd5ed-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fd5ed-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="fd5ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fd5ed-107">DESCRIPTION</span></span>
<span data-ttu-id="fd5ed-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** pobiera szczegóły mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="fd5ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd5ed-109">EXAMPLES</span></span>

### <span data-ttu-id="fd5ed-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd5ed-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="fd5ed-111">Wyświetl wszystkie mapowania klasyfikacji magazynu odpowiadające określonej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="fd5ed-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd5ed-112">PARAMETERS</span></span>

### <span data-ttu-id="fd5ed-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd5ed-113">-Name</span></span>
<span data-ttu-id="fd5ed-114">Określa nazwę mapowania klasyfikacji magazynu, które ma zostać odzyskane.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-114">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5ed-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="fd5ed-115">-StorageClassification</span></span>
<span data-ttu-id="fd5ed-116">Określa obiekt klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="fd5ed-117">Polecenie cmdlet pobiera mapowania klasyfikacji magazynu ASR odpowiadające określonej klasyfikacji magazynu</span><span class="sxs-lookup"><span data-stu-id="fd5ed-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="fd5ed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5ed-118">CommonParameters</span></span>
<span data-ttu-id="fd5ed-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5ed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5ed-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd5ed-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5ed-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd5ed-121">INPUTS</span></span>

### <span data-ttu-id="fd5ed-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fd5ed-122">None</span></span>

## <span data-ttu-id="fd5ed-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd5ed-123">OUTPUTS</span></span>

### <span data-ttu-id="fd5ed-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd5ed-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd5ed-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd5ed-125">NOTES</span></span>

## <span data-ttu-id="fd5ed-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd5ed-126">RELATED LINKS</span></span>

[<span data-ttu-id="fd5ed-127">Nowe — AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd5ed-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="fd5ed-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="fd5ed-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553136"
---
# <span data-ttu-id="2e1f8-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2e1f8-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2e1f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1f8-103">Pobiera dostępne (odnalezione) klasyfikacje magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e1f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e1f8-104">SYNTAX</span></span>

### <span data-ttu-id="2e1f8-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e1f8-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="2e1f8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2e1f8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="2e1f8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2e1f8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="2e1f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e1f8-108">DESCRIPTION</span></span>
<span data-ttu-id="2e1f8-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassification** pobiera szczegóły odnalezionych klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2e1f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e1f8-110">EXAMPLES</span></span>

### <span data-ttu-id="2e1f8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e1f8-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2e1f8-112">Lista odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2e1f8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e1f8-113">PARAMETERS</span></span>

### <span data-ttu-id="2e1f8-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="2e1f8-114">-Fabric</span></span>
<span data-ttu-id="2e1f8-115">Określa obiekt sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2e1f8-116">Polecenie cmdlet umożliwia pobieranie szczegółów dotyczących odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1f8-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2e1f8-117">-FriendlyName</span></span>
<span data-ttu-id="2e1f8-118">Określa przyjazną nazwę obiektu klasyfikacji magazynu, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-118">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1f8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e1f8-119">-Name</span></span>
<span data-ttu-id="2e1f8-120">Określa nazwę obiektu klasyfikacji magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2e1f8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1f8-121">CommonParameters</span></span>
<span data-ttu-id="2e1f8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1f8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1f8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e1f8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1f8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e1f8-124">INPUTS</span></span>

### <span data-ttu-id="2e1f8-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2e1f8-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2e1f8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e1f8-126">OUTPUTS</span></span>

### <span data-ttu-id="2e1f8-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2e1f8-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2e1f8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e1f8-128">NOTES</span></span>

## <span data-ttu-id="2e1f8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e1f8-129">RELATED LINKS</span></span>


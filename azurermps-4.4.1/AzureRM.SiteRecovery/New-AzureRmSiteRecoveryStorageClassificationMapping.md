---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527262"
---
# <span data-ttu-id="5ae99-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5ae99-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="5ae99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ae99-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae99-103">Tworzy mapowanie klasyfikacji magazynu w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="5ae99-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ae99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ae99-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ae99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ae99-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae99-106">Polecenie cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5ae99-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="5ae99-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ae99-107">EXAMPLES</span></span>

## <span data-ttu-id="5ae99-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ae99-108">PARAMETERS</span></span>

### <span data-ttu-id="5ae99-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ae99-109">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae99-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5ae99-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="5ae99-111">Określa mapowanie podstawowej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ae99-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae99-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5ae99-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="5ae99-113">Określa mapowanie klasyfikacji magazynu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5ae99-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae99-114">-DefaultProfile</span></span>
<span data-ttu-id="5ae99-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ae99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ae99-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae99-116">CommonParameters</span></span>
<span data-ttu-id="5ae99-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae99-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae99-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae99-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae99-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ae99-119">INPUTS</span></span>

### <span data-ttu-id="5ae99-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="5ae99-120">ASRStorageClassification</span></span>
<span data-ttu-id="5ae99-121">Parametr "PrimaryStorageClassification" akceptuje wartość typu "ASRStorageClassification" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5ae99-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="5ae99-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ae99-122">OUTPUTS</span></span>

### <span data-ttu-id="5ae99-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5ae99-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5ae99-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ae99-124">NOTES</span></span>

## <span data-ttu-id="5ae99-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ae99-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ae99-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5ae99-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="5ae99-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5ae99-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)

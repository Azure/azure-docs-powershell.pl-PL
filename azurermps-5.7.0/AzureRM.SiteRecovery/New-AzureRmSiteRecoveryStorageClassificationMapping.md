---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542263"
---
# <span data-ttu-id="e3b05-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e3b05-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="e3b05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3b05-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b05-103">Tworzy mapowanie klasyfikacji magazynu w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="e3b05-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3b05-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3b05-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b05-106">Polecenie cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e3b05-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="e3b05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3b05-107">EXAMPLES</span></span>

## <span data-ttu-id="e3b05-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3b05-108">PARAMETERS</span></span>

### <span data-ttu-id="e3b05-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b05-109">-DefaultProfile</span></span>
<span data-ttu-id="e3b05-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b05-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b05-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3b05-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b05-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e3b05-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="e3b05-113">Określa mapowanie podstawowej klasyfikacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3b05-113">Specifies the primary storage classification mapping.</span></span>

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

### <span data-ttu-id="e3b05-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e3b05-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="e3b05-115">Określa mapowanie klasyfikacji magazynu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3b05-115">Specifies a recovery storage classification mapping.</span></span>

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

### <span data-ttu-id="e3b05-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b05-116">CommonParameters</span></span>
<span data-ttu-id="e3b05-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b05-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b05-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b05-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b05-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3b05-119">INPUTS</span></span>

### <span data-ttu-id="e3b05-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e3b05-120">ASRStorageClassification</span></span>
<span data-ttu-id="e3b05-121">Parametr "PrimaryStorageClassification" akceptuje wartość typu "ASRStorageClassification" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e3b05-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="e3b05-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3b05-122">OUTPUTS</span></span>

### <span data-ttu-id="e3b05-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e3b05-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e3b05-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3b05-124">NOTES</span></span>

## <span data-ttu-id="e3b05-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3b05-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3b05-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e3b05-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="e3b05-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e3b05-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)

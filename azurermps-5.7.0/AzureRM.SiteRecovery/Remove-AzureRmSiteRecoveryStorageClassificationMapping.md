---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547932"
---
# <span data-ttu-id="b1fb3-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b1fb3-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="b1fb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fb3-103">Usuwa mapowanie klasyfikacji magazynu z odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1fb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1fb3-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1fb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="b1fb3-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** usuwa mapowanie klasyfikacji magazynu z usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="b1fb3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1fb3-107">EXAMPLES</span></span>

## <span data-ttu-id="b1fb3-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1fb3-108">PARAMETERS</span></span>

### <span data-ttu-id="b1fb3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fb3-109">-DefaultProfile</span></span>
<span data-ttu-id="b1fb3-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1fb3-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b1fb3-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="b1fb3-112">Określa mapowanie klasyfikacji magazynu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fb3-113">CommonParameters</span></span>
<span data-ttu-id="b1fb3-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fb3-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fb3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fb3-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1fb3-116">INPUTS</span></span>

### <span data-ttu-id="b1fb3-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b1fb3-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="b1fb3-118">Parametr "StorageClassificationMapping" akceptuje wartość typu "ASRStorageClassificationMapping" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b1fb3-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="b1fb3-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1fb3-119">OUTPUTS</span></span>

### <span data-ttu-id="b1fb3-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b1fb3-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b1fb3-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1fb3-121">NOTES</span></span>

## <span data-ttu-id="b1fb3-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1fb3-122">RELATED LINKS</span></span>

[<span data-ttu-id="b1fb3-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b1fb3-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="b1fb3-124">Nowe — AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b1fb3-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

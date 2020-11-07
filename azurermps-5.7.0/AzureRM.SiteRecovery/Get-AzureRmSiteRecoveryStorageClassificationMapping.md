---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718443"
---
# <span data-ttu-id="f2a67-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2a67-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="f2a67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2a67-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a67-103">Pobiera mapowanie klasyfikacji magazynu w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="f2a67-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2a67-104">SYNTAX</span></span>

### <span data-ttu-id="f2a67-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f2a67-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2a67-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f2a67-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2a67-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f2a67-107">DESCRIPTION</span></span>
<span data-ttu-id="f2a67-108">Polecenie cmdlet **Get-AzureRmSiteRecoveryStorageClassificationMapping** pobiera mapowanie klasyfikacji magazynu w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f2a67-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="f2a67-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2a67-109">EXAMPLES</span></span>

## <span data-ttu-id="f2a67-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2a67-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a67-111">-DefaultProfile</span></span>
<span data-ttu-id="f2a67-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2a67-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2a67-113">-Name</span></span>
<span data-ttu-id="f2a67-114">Określa nazwę mapowania klasyfikacji magazynu, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2a67-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a67-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a67-115">CommonParameters</span></span>
<span data-ttu-id="f2a67-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a67-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a67-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a67-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a67-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2a67-118">INPUTS</span></span>

### <span data-ttu-id="f2a67-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2a67-119">None</span></span>
<span data-ttu-id="f2a67-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f2a67-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2a67-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2a67-121">OUTPUTS</span></span>

### <span data-ttu-id="f2a67-122">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="f2a67-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="f2a67-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2a67-123">NOTES</span></span>

## <span data-ttu-id="f2a67-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2a67-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2a67-125">Nowe — AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2a67-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="f2a67-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f2a67-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)

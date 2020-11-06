---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551560"
---
# <span data-ttu-id="0eb1d-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0eb1d-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="0eb1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0eb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb1d-103">Pobiera mapowania kontenerów ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eb1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0eb1d-104">SYNTAX</span></span>

### <span data-ttu-id="0eb1d-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0eb1d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eb1d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0eb1d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eb1d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0eb1d-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb1d-108">Polecenie cmdlet **Get-AzureRmSiteRecoveryProtectionContainerMapping** pobiera informacje o kontenerze ochrony do mapowań zasad w magazynie.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="0eb1d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0eb1d-109">EXAMPLES</span></span>

## <span data-ttu-id="0eb1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0eb1d-110">PARAMETERS</span></span>

### <span data-ttu-id="0eb1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb1d-111">-DefaultProfile</span></span>
<span data-ttu-id="0eb1d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb1d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0eb1d-113">-Name</span></span>
<span data-ttu-id="0eb1d-114">Określa nazwę mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="0eb1d-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0eb1d-115">-ProtectionContainer</span></span>
<span data-ttu-id="0eb1d-116">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb1d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb1d-117">CommonParameters</span></span>
<span data-ttu-id="0eb1d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb1d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb1d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb1d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb1d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb1d-120">INPUTS</span></span>

### <span data-ttu-id="0eb1d-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0eb1d-121">ASRProtectionContainer</span></span>
<span data-ttu-id="0eb1d-122">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0eb1d-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="0eb1d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0eb1d-123">OUTPUTS</span></span>

### <span data-ttu-id="0eb1d-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0eb1d-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0eb1d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0eb1d-125">NOTES</span></span>

## <span data-ttu-id="0eb1d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eb1d-126">RELATED LINKS</span></span>

[<span data-ttu-id="0eb1d-127">Nowe — AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0eb1d-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="0eb1d-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0eb1d-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)

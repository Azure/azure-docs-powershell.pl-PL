---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718981"
---
# <span data-ttu-id="5b384-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5b384-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="5b384-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b384-102">SYNOPSIS</span></span>
<span data-ttu-id="5b384-103">Tworzy sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="5b384-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b384-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b384-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b384-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b384-105">DESCRIPTION</span></span>
<span data-ttu-id="5b384-106">Polecenie cmdlet **New-AzureRmSiteRecoveryFabric** umożliwia utworzenie sieci szkieletowej odzyskiwania witryny platformy Azure określonego typu.</span><span class="sxs-lookup"><span data-stu-id="5b384-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="5b384-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b384-107">EXAMPLES</span></span>

## <span data-ttu-id="5b384-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b384-108">PARAMETERS</span></span>

### <span data-ttu-id="5b384-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b384-109">-Name</span></span>
<span data-ttu-id="5b384-110">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure</span><span class="sxs-lookup"><span data-stu-id="5b384-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b384-111">-Type</span><span class="sxs-lookup"><span data-stu-id="5b384-111">-Type</span></span>
<span data-ttu-id="5b384-112">Określa typ sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5b384-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b384-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b384-113">-DefaultProfile</span></span>
<span data-ttu-id="5b384-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b384-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b384-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b384-115">CommonParameters</span></span>
<span data-ttu-id="5b384-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b384-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b384-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b384-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b384-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b384-118">INPUTS</span></span>

## <span data-ttu-id="5b384-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b384-119">OUTPUTS</span></span>

### <span data-ttu-id="5b384-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5b384-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5b384-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b384-121">NOTES</span></span>

## <span data-ttu-id="5b384-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b384-122">RELATED LINKS</span></span>

[<span data-ttu-id="5b384-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5b384-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="5b384-124">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5b384-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551516"
---
# <span data-ttu-id="90566-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="90566-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="90566-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90566-102">SYNOPSIS</span></span>
<span data-ttu-id="90566-103">Usuwa mapowanie sieci z bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="90566-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90566-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90566-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90566-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90566-105">DESCRIPTION</span></span>
<span data-ttu-id="90566-106">Polecenie cmdlet **Remove-AzureRMSiteRecoveryNetworkMapping** usuwa mapowanie sieci z bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="90566-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="90566-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90566-107">EXAMPLES</span></span>

## <span data-ttu-id="90566-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90566-108">PARAMETERS</span></span>

### <span data-ttu-id="90566-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90566-109">-DefaultProfile</span></span>
<span data-ttu-id="90566-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90566-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90566-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="90566-111">-NetworkMapping</span></span>
<span data-ttu-id="90566-112">Określa obiekt mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="90566-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90566-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90566-113">CommonParameters</span></span>
<span data-ttu-id="90566-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90566-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90566-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90566-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90566-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90566-116">INPUTS</span></span>

### <span data-ttu-id="90566-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="90566-117">ASRNetworkMapping</span></span>
<span data-ttu-id="90566-118">Parametr "NetworkMapping" akceptuje wartość typu "ASRNetworkMapping" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="90566-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="90566-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90566-119">OUTPUTS</span></span>

### <span data-ttu-id="90566-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="90566-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90566-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90566-121">NOTES</span></span>

## <span data-ttu-id="90566-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90566-122">RELATED LINKS</span></span>

[<span data-ttu-id="90566-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="90566-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="90566-124">Nowe — AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="90566-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

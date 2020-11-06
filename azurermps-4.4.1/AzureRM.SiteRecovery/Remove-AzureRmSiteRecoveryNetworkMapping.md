---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 03bd15f1071ac223ba7460c27bcfd9ce96a55dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545988"
---
# <span data-ttu-id="bd466-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bd466-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="bd466-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd466-102">SYNOPSIS</span></span>
<span data-ttu-id="bd466-103">Usuwa mapowanie sieci z bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="bd466-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd466-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd466-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd466-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd466-105">DESCRIPTION</span></span>
<span data-ttu-id="bd466-106">Polecenie cmdlet **Remove-AzureRMSiteRecoveryNetworkMapping** usuwa mapowanie sieci z bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bd466-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="bd466-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd466-107">EXAMPLES</span></span>

## <span data-ttu-id="bd466-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd466-108">PARAMETERS</span></span>

### <span data-ttu-id="bd466-109">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bd466-109">-NetworkMapping</span></span>
<span data-ttu-id="bd466-110">Określa obiekt mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="bd466-110">Specifies the network mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd466-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd466-111">-DefaultProfile</span></span>
<span data-ttu-id="bd466-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd466-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd466-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd466-113">CommonParameters</span></span>
<span data-ttu-id="bd466-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd466-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd466-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd466-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd466-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd466-116">INPUTS</span></span>

### <span data-ttu-id="bd466-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bd466-117">ASRNetworkMapping</span></span>
<span data-ttu-id="bd466-118">Parametr "NetworkMapping" akceptuje wartość typu "ASRNetworkMapping" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bd466-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="bd466-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd466-119">OUTPUTS</span></span>

### <span data-ttu-id="bd466-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bd466-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd466-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd466-121">NOTES</span></span>

## <span data-ttu-id="bd466-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd466-122">RELATED LINKS</span></span>

[<span data-ttu-id="bd466-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bd466-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="bd466-124">Nowe — AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bd466-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719267"
---
# <span data-ttu-id="752df-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="752df-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="752df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="752df-102">SYNOPSIS</span></span>
<span data-ttu-id="752df-103">Pobiera informacje o mapowaniach sieciowych odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="752df-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="752df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="752df-104">SYNTAX</span></span>

### <span data-ttu-id="752df-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="752df-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="752df-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="752df-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="752df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="752df-107">DESCRIPTION</span></span>
<span data-ttu-id="752df-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="752df-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="752df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="752df-109">EXAMPLES</span></span>

### <span data-ttu-id="752df-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="752df-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="752df-111">Pobiera wszystkie mapowania sieci dla przekazanej sieci.</span><span class="sxs-lookup"><span data-stu-id="752df-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="752df-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="752df-112">PARAMETERS</span></span>

### <span data-ttu-id="752df-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="752df-113">-Name</span></span>
<span data-ttu-id="752df-114">Nazwa obiektu mapowania sieci funkcji ASR do pobrania.</span><span class="sxs-lookup"><span data-stu-id="752df-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="752df-115">-Network</span><span class="sxs-lookup"><span data-stu-id="752df-115">-Network</span></span>
<span data-ttu-id="752df-116">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu obiektowi sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="752df-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="752df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752df-117">CommonParameters</span></span>
<span data-ttu-id="752df-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752df-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752df-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="752df-120">INPUTS</span></span>

### <span data-ttu-id="752df-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="752df-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="752df-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="752df-122">OUTPUTS</span></span>

### <span data-ttu-id="752df-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="752df-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="752df-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="752df-124">NOTES</span></span>

## <span data-ttu-id="752df-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="752df-125">RELATED LINKS</span></span>

[<span data-ttu-id="752df-126">Nowe — AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="752df-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="752df-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="752df-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550823"
---
# <span data-ttu-id="81b9a-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81b9a-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="81b9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="81b9a-103">Umożliwia zaktualizowanie określonego mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="81b9a-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81b9a-104">SYNTAX</span></span>

### <span data-ttu-id="81b9a-105">ByNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81b9a-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81b9a-106">ById</span><span class="sxs-lookup"><span data-stu-id="81b9a-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b9a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="81b9a-107">DESCRIPTION</span></span>
<span data-ttu-id="81b9a-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aktualizuje określone mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="81b9a-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="81b9a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81b9a-109">EXAMPLES</span></span>

### <span data-ttu-id="81b9a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81b9a-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="81b9a-111">Rozpoczyna operację aktualizowania mapowania sieci przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="81b9a-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="81b9a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81b9a-112">PARAMETERS</span></span>

### <span data-ttu-id="81b9a-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81b9a-113">-InputObject</span></span>
<span data-ttu-id="81b9a-114">Obiekt wejściowy: określa obiekt mapowania sieci funkcji ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać zaktualizowany</span><span class="sxs-lookup"><span data-stu-id="81b9a-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81b9a-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="81b9a-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="81b9a-116">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="81b9a-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b9a-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="81b9a-117">-RecoveryNetwork</span></span>
<span data-ttu-id="81b9a-118">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="81b9a-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b9a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81b9a-119">-Confirm</span></span>
<span data-ttu-id="81b9a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b9a-121">-WhatIf</span></span>
<span data-ttu-id="81b9a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b9a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81b9a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81b9a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b9a-124">CommonParameters</span></span>
<span data-ttu-id="81b9a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b9a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b9a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b9a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81b9a-127">INPUTS</span></span>

### <span data-ttu-id="81b9a-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="81b9a-128">None</span></span>

## <span data-ttu-id="81b9a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81b9a-129">OUTPUTS</span></span>

### <span data-ttu-id="81b9a-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="81b9a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81b9a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81b9a-131">NOTES</span></span>

## <span data-ttu-id="81b9a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81b9a-132">RELATED LINKS</span></span>


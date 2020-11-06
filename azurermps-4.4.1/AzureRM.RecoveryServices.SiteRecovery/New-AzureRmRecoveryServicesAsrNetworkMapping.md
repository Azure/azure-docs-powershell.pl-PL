---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550835"
---
# <span data-ttu-id="c5497-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c5497-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c5497-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5497-102">SYNOPSIS</span></span>
<span data-ttu-id="c5497-103">Tworzy mapowanie sieci funkcji ASR między dwiema sieciami.</span><span class="sxs-lookup"><span data-stu-id="c5497-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5497-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5497-104">SYNTAX</span></span>

### <span data-ttu-id="c5497-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5497-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5497-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c5497-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5497-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5497-107">DESCRIPTION</span></span>
<span data-ttu-id="c5497-108">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** uruchamia operację tworzenia mapowania sieciowego funkcji ASR między dwiema sieciami i zwraca obiekt zadania ASR dla zadania ASR użytego do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c5497-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c5497-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5497-109">EXAMPLES</span></span>

### <span data-ttu-id="c5497-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5497-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="c5497-111">Rozpoczyna operację tworzenia mapowania sieci przy użyciu określonej nazwy, sieci podstawowej i sieci odzyskiwania, a następnie zwraca zadanie ASR, aby śledzić operację.</span><span class="sxs-lookup"><span data-stu-id="c5497-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="c5497-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5497-112">PARAMETERS</span></span>

### <span data-ttu-id="c5497-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5497-113">-Name</span></span>
<span data-ttu-id="c5497-114">Nazwa mapowania sieci funkcji ASR do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="c5497-114">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5497-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c5497-115">-PrimaryNetwork</span></span>
<span data-ttu-id="c5497-116">Określa podstawowy obiekt sieciowy dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="c5497-116">Specifies the primary network object for the network mapping.</span></span>

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

### <span data-ttu-id="c5497-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c5497-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="c5497-118">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="c5497-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5497-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c5497-119">-RecoveryNetwork</span></span>
<span data-ttu-id="c5497-120">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="c5497-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5497-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5497-121">-Confirm</span></span>
<span data-ttu-id="c5497-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5497-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5497-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5497-123">-WhatIf</span></span>
<span data-ttu-id="c5497-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5497-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5497-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c5497-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5497-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5497-126">CommonParameters</span></span>
<span data-ttu-id="c5497-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5497-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5497-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5497-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5497-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5497-129">INPUTS</span></span>

### <span data-ttu-id="c5497-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c5497-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c5497-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5497-131">OUTPUTS</span></span>

### <span data-ttu-id="c5497-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c5497-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c5497-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5497-133">NOTES</span></span>

## <span data-ttu-id="c5497-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5497-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5497-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c5497-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c5497-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c5497-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)

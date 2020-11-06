---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524993"
---
# <span data-ttu-id="70b81-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="70b81-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="70b81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70b81-102">SYNOPSIS</span></span>
<span data-ttu-id="70b81-103">Umożliwia zaktualizowanie określonego mapowania sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="70b81-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70b81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70b81-104">SYNTAX</span></span>

### <span data-ttu-id="70b81-105">ByNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70b81-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70b81-106">ById</span><span class="sxs-lookup"><span data-stu-id="70b81-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70b81-107">Opis</span><span class="sxs-lookup"><span data-stu-id="70b81-107">DESCRIPTION</span></span>
<span data-ttu-id="70b81-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aktualizuje określone mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="70b81-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="70b81-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70b81-109">EXAMPLES</span></span>

### <span data-ttu-id="70b81-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70b81-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="70b81-111">Rozpoczyna operację aktualizowania mapowania sieci przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="70b81-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="70b81-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70b81-112">PARAMETERS</span></span>

### <span data-ttu-id="70b81-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70b81-113">-Confirm</span></span>
<span data-ttu-id="70b81-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70b81-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b81-115">-DefaultProfile</span></span>
<span data-ttu-id="70b81-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70b81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="70b81-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70b81-117">-InputObject</span></span>
<span data-ttu-id="70b81-118">Obiekt wejściowy: określa obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="70b81-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="70b81-119">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="70b81-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="70b81-120">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="70b81-120">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="70b81-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="70b81-121">-RecoveryNetwork</span></span>
<span data-ttu-id="70b81-122">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="70b81-122">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="70b81-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b81-123">-WhatIf</span></span>
<span data-ttu-id="70b81-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70b81-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70b81-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70b81-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b81-126">CommonParameters</span></span>
<span data-ttu-id="70b81-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b81-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b81-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70b81-129">INPUTS</span></span>

### <span data-ttu-id="70b81-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70b81-130">None</span></span>

## <span data-ttu-id="70b81-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70b81-131">OUTPUTS</span></span>

### <span data-ttu-id="70b81-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="70b81-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70b81-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70b81-133">NOTES</span></span>

## <span data-ttu-id="70b81-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70b81-134">RELATED LINKS</span></span>

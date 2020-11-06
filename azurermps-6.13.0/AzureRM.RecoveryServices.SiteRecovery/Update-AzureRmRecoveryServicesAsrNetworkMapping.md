---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: fb92ec38bcbe7addb23f274616cde0fd84ebbafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526106"
---
# <span data-ttu-id="10479-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="10479-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="10479-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10479-102">SYNOPSIS</span></span>
<span data-ttu-id="10479-103">Umożliwia zaktualizowanie określonego mapowania sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10479-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10479-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10479-104">SYNTAX</span></span>

### <span data-ttu-id="10479-105">ByNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10479-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10479-106">ById</span><span class="sxs-lookup"><span data-stu-id="10479-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10479-107">Opis</span><span class="sxs-lookup"><span data-stu-id="10479-107">DESCRIPTION</span></span>
<span data-ttu-id="10479-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aktualizuje określone mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10479-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="10479-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10479-109">EXAMPLES</span></span>

### <span data-ttu-id="10479-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10479-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="10479-111">Rozpoczyna operację aktualizowania mapowania sieci przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="10479-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="10479-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10479-112">PARAMETERS</span></span>

### <span data-ttu-id="10479-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10479-113">-DefaultProfile</span></span>
<span data-ttu-id="10479-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10479-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="10479-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10479-115">-InputObject</span></span>
<span data-ttu-id="10479-116">Obiekt wejściowy: określa obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="10479-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10479-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="10479-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="10479-118">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="10479-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10479-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="10479-119">-RecoveryNetwork</span></span>
<span data-ttu-id="10479-120">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="10479-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10479-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10479-121">-Confirm</span></span>
<span data-ttu-id="10479-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10479-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10479-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10479-123">-WhatIf</span></span>
<span data-ttu-id="10479-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10479-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10479-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10479-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10479-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10479-126">CommonParameters</span></span>
<span data-ttu-id="10479-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10479-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10479-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10479-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10479-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10479-129">INPUTS</span></span>

### <span data-ttu-id="10479-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="10479-130">None</span></span>

## <span data-ttu-id="10479-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10479-131">OUTPUTS</span></span>

### <span data-ttu-id="10479-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10479-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10479-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10479-133">NOTES</span></span>

## <span data-ttu-id="10479-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10479-134">RELATED LINKS</span></span>

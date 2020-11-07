---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 32412127388e233af303cc29de8ecf66304a0bf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708545"
---
# <span data-ttu-id="381a7-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="381a7-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="381a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="381a7-102">SYNOPSIS</span></span>
<span data-ttu-id="381a7-103">Umożliwia zaktualizowanie określonego mapowania sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="381a7-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="381a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="381a7-104">SYNTAX</span></span>

### <span data-ttu-id="381a7-105">ByNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="381a7-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="381a7-106">ById</span><span class="sxs-lookup"><span data-stu-id="381a7-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381a7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="381a7-107">DESCRIPTION</span></span>
<span data-ttu-id="381a7-108">Polecenie cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** aktualizuje określone mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="381a7-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="381a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="381a7-109">EXAMPLES</span></span>

### <span data-ttu-id="381a7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="381a7-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="381a7-111">Rozpoczyna operację aktualizowania mapowania sieci przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="381a7-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="381a7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="381a7-112">PARAMETERS</span></span>

### <span data-ttu-id="381a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381a7-113">-DefaultProfile</span></span>
<span data-ttu-id="381a7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="381a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381a7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="381a7-115">-InputObject</span></span>
<span data-ttu-id="381a7-116">Obiekt wejściowy: określa obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="381a7-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="381a7-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="381a7-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="381a7-118">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="381a7-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="381a7-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="381a7-119">-RecoveryNetwork</span></span>
<span data-ttu-id="381a7-120">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="381a7-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="381a7-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="381a7-121">-Confirm</span></span>
<span data-ttu-id="381a7-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="381a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381a7-123">-WhatIf</span></span>
<span data-ttu-id="381a7-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="381a7-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="381a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="381a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381a7-126">CommonParameters</span></span>
<span data-ttu-id="381a7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381a7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381a7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="381a7-129">INPUTS</span></span>

### <span data-ttu-id="381a7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="381a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="381a7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="381a7-131">OUTPUTS</span></span>

### <span data-ttu-id="381a7-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="381a7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="381a7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="381a7-133">NOTES</span></span>

## <span data-ttu-id="381a7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="381a7-134">RELATED LINKS</span></span>

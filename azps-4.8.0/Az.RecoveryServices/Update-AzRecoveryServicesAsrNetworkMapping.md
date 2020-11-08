---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219972"
---
# <span data-ttu-id="32c53-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="32c53-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="32c53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32c53-102">SYNOPSIS</span></span>
<span data-ttu-id="32c53-103">Umożliwia zaktualizowanie określonego mapowania sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="32c53-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="32c53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32c53-104">SYNTAX</span></span>

### <span data-ttu-id="32c53-105">ByNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32c53-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c53-106">ById</span><span class="sxs-lookup"><span data-stu-id="32c53-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32c53-107">Opis</span><span class="sxs-lookup"><span data-stu-id="32c53-107">DESCRIPTION</span></span>
<span data-ttu-id="32c53-108">Polecenie cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** aktualizuje określone mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="32c53-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="32c53-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32c53-109">EXAMPLES</span></span>

### <span data-ttu-id="32c53-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32c53-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="32c53-111">Rozpoczyna operację aktualizowania mapowania sieci przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="32c53-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="32c53-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32c53-112">PARAMETERS</span></span>

### <span data-ttu-id="32c53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c53-113">-DefaultProfile</span></span>
<span data-ttu-id="32c53-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32c53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="32c53-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32c53-115">-InputObject</span></span>
<span data-ttu-id="32c53-116">Obiekt wejściowy: określa obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="32c53-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="32c53-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="32c53-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="32c53-118">Określa identyfikator sieci Azure służący do odzyskania mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="32c53-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="32c53-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="32c53-119">-RecoveryNetwork</span></span>
<span data-ttu-id="32c53-120">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="32c53-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="32c53-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32c53-121">-Confirm</span></span>
<span data-ttu-id="32c53-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c53-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c53-123">-WhatIf</span></span>
<span data-ttu-id="32c53-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c53-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32c53-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32c53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c53-126">CommonParameters</span></span>
<span data-ttu-id="32c53-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c53-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32c53-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c53-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32c53-129">INPUTS</span></span>

### <span data-ttu-id="32c53-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="32c53-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="32c53-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32c53-131">OUTPUTS</span></span>

### <span data-ttu-id="32c53-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="32c53-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="32c53-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32c53-133">NOTES</span></span>

## <span data-ttu-id="32c53-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32c53-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 6041973d4bab91310ed213d461cf97db9cc5e720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993497"
---
# <span data-ttu-id="71ab5-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="71ab5-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="71ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="71ab5-103">Aktualizuje wskazane mapowanie sieci odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71ab5-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="71ab5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71ab5-104">SYNTAX</span></span>

### <span data-ttu-id="71ab5-105">ByNetworkObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="71ab5-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ab5-106">ById</span><span class="sxs-lookup"><span data-stu-id="71ab5-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ab5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="71ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="71ab5-108">Polecenie **cmdlet Update-AzRecoveryServicesAsrNetworkMapping** aktualizuje wskazane mapowanie sieci usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71ab5-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="71ab5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71ab5-109">EXAMPLES</span></span>

### <span data-ttu-id="71ab5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71ab5-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="71ab5-111">Uruchamia operację mapowania sieci aktualizacji przy użyciu określonych parametrów i zwraca zadanie funkcji ASR służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="71ab5-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="71ab5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71ab5-112">PARAMETERS</span></span>

### <span data-ttu-id="71ab5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ab5-113">-DefaultProfile</span></span>
<span data-ttu-id="71ab5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71ab5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71ab5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71ab5-115">-InputObject</span></span>
<span data-ttu-id="71ab5-116">Obiekt wejściowy: określa obiekt mapowania sieci ASR odpowiadający zaktualizowanej funkcji mapowania sieci asr.</span><span class="sxs-lookup"><span data-stu-id="71ab5-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="71ab5-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="71ab5-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="71ab5-118">Określa identyfikator sieci azure odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="71ab5-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="71ab5-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="71ab5-119">-RecoveryNetwork</span></span>
<span data-ttu-id="71ab5-120">Określa obiekt sieci odzyskiwania dla mapowania sieci.</span><span class="sxs-lookup"><span data-stu-id="71ab5-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="71ab5-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71ab5-121">-Confirm</span></span>
<span data-ttu-id="71ab5-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71ab5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ab5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ab5-123">-WhatIf</span></span>
<span data-ttu-id="71ab5-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71ab5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71ab5-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="71ab5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ab5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ab5-126">CommonParameters</span></span>
<span data-ttu-id="71ab5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ab5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ab5-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71ab5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ab5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71ab5-129">INPUTS</span></span>

### <span data-ttu-id="71ab5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="71ab5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="71ab5-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71ab5-131">OUTPUTS</span></span>

### <span data-ttu-id="71ab5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="71ab5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71ab5-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71ab5-133">NOTES</span></span>

## <span data-ttu-id="71ab5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71ab5-134">RELATED LINKS</span></span>

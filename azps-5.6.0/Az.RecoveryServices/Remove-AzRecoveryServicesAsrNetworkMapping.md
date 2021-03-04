---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: bb80bebc8c1a5dccbeedf4abd277891c3b2e9de7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953281"
---
# <span data-ttu-id="6f386-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6f386-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6f386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f386-102">SYNOPSIS</span></span>
<span data-ttu-id="6f386-103">Usuwa wskazane mapowanie sieci asr z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6f386-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="6f386-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6f386-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f386-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6f386-105">DESCRIPTION</span></span>
<span data-ttu-id="6f386-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrNetworkMapping** usuwa wskazane mapowanie sieci asr.</span><span class="sxs-lookup"><span data-stu-id="6f386-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="6f386-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6f386-107">EXAMPLES</span></span>

### <span data-ttu-id="6f386-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f386-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="6f386-109">Rozpoczyna usuwanie określonego mapowania sieci asr i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6f386-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6f386-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f386-110">PARAMETERS</span></span>

### <span data-ttu-id="6f386-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f386-111">-DefaultProfile</span></span>
<span data-ttu-id="6f386-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f386-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6f386-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f386-113">-InputObject</span></span>
<span data-ttu-id="6f386-114">Obiekt wejściowy do polecenia cmdlet: Obiekt mapowania sieci ASR odpowiadający mapowaniu sieci asr do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6f386-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="6f386-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f386-115">-Confirm</span></span>
<span data-ttu-id="6f386-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6f386-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f386-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f386-117">-WhatIf</span></span>
<span data-ttu-id="6f386-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f386-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f386-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6f386-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f386-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f386-120">CommonParameters</span></span>
<span data-ttu-id="6f386-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f386-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f386-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f386-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f386-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f386-123">INPUTS</span></span>

### <span data-ttu-id="6f386-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6f386-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="6f386-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f386-125">OUTPUTS</span></span>

### <span data-ttu-id="6f386-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6f386-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6f386-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6f386-127">NOTES</span></span>

## <span data-ttu-id="6f386-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f386-128">RELATED LINKS</span></span>

[<span data-ttu-id="6f386-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6f386-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6f386-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6f386-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

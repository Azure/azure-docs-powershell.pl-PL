---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953258"
---
# <span data-ttu-id="cf92f-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cf92f-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="cf92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf92f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf92f-103">Usuwa określony kontener ochrony z jego struktury szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="cf92f-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="cf92f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf92f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf92f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf92f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf92f-106">Polecenie Remove-AzRecoveryServicesAsrProtectionContainer cmdlet usuwa określony kontener usługi Azure Site Recovery Protection.</span><span class="sxs-lookup"><span data-stu-id="cf92f-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="cf92f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf92f-107">EXAMPLES</span></span>

### <span data-ttu-id="cf92f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf92f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="cf92f-109">Rozpoczyna usuwanie określonego kontenera ochrony i zwraca zadanie asr służące do śledzenia operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="cf92f-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="cf92f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf92f-110">PARAMETERS</span></span>

### <span data-ttu-id="cf92f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf92f-111">-DefaultProfile</span></span>
<span data-ttu-id="cf92f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf92f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf92f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf92f-113">-InputObject</span></span>
<span data-ttu-id="cf92f-114">Określa kontener ochrony do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cf92f-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf92f-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf92f-115">-Confirm</span></span>
<span data-ttu-id="cf92f-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf92f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf92f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf92f-117">-WhatIf</span></span>
<span data-ttu-id="cf92f-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf92f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf92f-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf92f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf92f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf92f-120">CommonParameters</span></span>
<span data-ttu-id="cf92f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf92f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf92f-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf92f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf92f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf92f-123">INPUTS</span></span>

### <span data-ttu-id="cf92f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cf92f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="cf92f-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf92f-125">OUTPUTS</span></span>

### <span data-ttu-id="cf92f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cf92f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cf92f-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf92f-127">NOTES</span></span>

## <span data-ttu-id="cf92f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf92f-128">RELATED LINKS</span></span>

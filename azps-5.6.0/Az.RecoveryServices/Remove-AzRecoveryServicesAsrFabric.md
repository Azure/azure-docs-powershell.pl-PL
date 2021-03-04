---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: ed06852e2ce0342502d01bd7f5ae17c0c3b8f4e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953290"
---
# <span data-ttu-id="e5035-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e5035-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="e5035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5035-102">SYNOPSIS</span></span>
<span data-ttu-id="e5035-103">Usuwa określoną sieć Azure Site Recovery Fabric z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e5035-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="e5035-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5035-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5035-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5035-105">DESCRIPTION</span></span>
<span data-ttu-id="e5035-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową usługi Azure Site Recovery z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e5035-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="e5035-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5035-107">EXAMPLES</span></span>

### <span data-ttu-id="e5035-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5035-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="e5035-109">Rozpoczyna usuwanie określonego materiału i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e5035-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e5035-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5035-110">PARAMETERS</span></span>

### <span data-ttu-id="e5035-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5035-111">-DefaultProfile</span></span>
<span data-ttu-id="e5035-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5035-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5035-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e5035-113">-Force</span></span>
<span data-ttu-id="e5035-114">Wymusz uruchomienie polecenia bez podaniem dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="e5035-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5035-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5035-115">-InputObject</span></span>
<span data-ttu-id="e5035-116">Obiekt wejściowy do polecenia cmdlet: obiekt z materiału ASR odpowiadający materiałowi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e5035-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5035-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5035-117">-Confirm</span></span>
<span data-ttu-id="e5035-118">Określ, czy jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5035-118">Specify if confirmation is required.</span></span> <span data-ttu-id="e5035-119">Ustaw wartość parametru confirm w celu $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5035-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e5035-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5035-120">-WhatIf</span></span>
<span data-ttu-id="e5035-121">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie wykonane bez wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5035-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e5035-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5035-122">CommonParameters</span></span>
<span data-ttu-id="e5035-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5035-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5035-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5035-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5035-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5035-125">INPUTS</span></span>

### <span data-ttu-id="e5035-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e5035-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e5035-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5035-127">OUTPUTS</span></span>

### <span data-ttu-id="e5035-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e5035-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e5035-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5035-129">NOTES</span></span>

## <span data-ttu-id="e5035-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5035-130">RELATED LINKS</span></span>

[<span data-ttu-id="e5035-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e5035-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="e5035-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e5035-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

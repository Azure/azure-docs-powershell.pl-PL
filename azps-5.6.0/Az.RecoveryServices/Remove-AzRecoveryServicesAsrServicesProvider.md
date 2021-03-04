---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953146"
---
# <span data-ttu-id="59c5e-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59c5e-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="59c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="59c5e-103">Usuwa/wyrejestrowywuje określonego dostawcę usług odzyskiwania witryny Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59c5e-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="59c5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59c5e-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c5e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="59c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="59c5e-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrServicesProvider** usuwa określonego dostawcę usług odzyskiwania witryny platformy Azure z magazynu.</span><span class="sxs-lookup"><span data-stu-id="59c5e-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="59c5e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="59c5e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59c5e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="59c5e-109">Uruchamia usuwanie/wyrejestrowanie określonego dostawcy usług Azure Site Recovery services i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="59c5e-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="59c5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c5e-110">PARAMETERS</span></span>

### <span data-ttu-id="59c5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c5e-111">-DefaultProfile</span></span>
<span data-ttu-id="59c5e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59c5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="59c5e-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="59c5e-113">-Force</span></span>
<span data-ttu-id="59c5e-114">Wymusz uruchomienie polecenia bez podaniem dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="59c5e-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="59c5e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c5e-115">-InputObject</span></span>
<span data-ttu-id="59c5e-116">Obiekt wejściowy do polecenia cmdlet: Obiekt dostawcy usług odzyskiwania ASR odpowiadający dostawcy usług odzyskiwania ASR do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="59c5e-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59c5e-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59c5e-117">-Confirm</span></span>
<span data-ttu-id="59c5e-118">Określ, czy jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59c5e-118">Specify if confirmation is required.</span></span> <span data-ttu-id="59c5e-119">Ustaw wartość parametru confirm w celu $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59c5e-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="59c5e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c5e-120">-WhatIf</span></span>
<span data-ttu-id="59c5e-121">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie wykonane bez wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59c5e-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="59c5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c5e-122">CommonParameters</span></span>
<span data-ttu-id="59c5e-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c5e-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59c5e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c5e-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59c5e-125">INPUTS</span></span>

### <span data-ttu-id="59c5e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59c5e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="59c5e-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59c5e-127">OUTPUTS</span></span>

### <span data-ttu-id="59c5e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="59c5e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="59c5e-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59c5e-129">NOTES</span></span>

## <span data-ttu-id="59c5e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59c5e-130">RELATED LINKS</span></span>

[<span data-ttu-id="59c5e-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59c5e-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="59c5e-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59c5e-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)

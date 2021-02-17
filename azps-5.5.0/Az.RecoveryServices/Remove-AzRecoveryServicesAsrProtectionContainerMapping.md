---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240267"
---
# <span data-ttu-id="a475a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a475a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="a475a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a475a-102">SYNOPSIS</span></span>
<span data-ttu-id="a475a-103">Usuwa wskazane mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a475a-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="a475a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a475a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a475a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a475a-105">DESCRIPTION</span></span>
<span data-ttu-id="a475a-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrProtectionContainerMapping** usuwa wskazane mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a475a-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="a475a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a475a-107">EXAMPLES</span></span>

### <span data-ttu-id="a475a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a475a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="a475a-109">Rozpoczyna usuwanie określonego mapowania kontenera ochrony i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a475a-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a475a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a475a-110">PARAMETERS</span></span>

### <span data-ttu-id="a475a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a475a-111">-DefaultProfile</span></span>
<span data-ttu-id="a475a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a475a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a475a-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a475a-113">-Force</span></span>
<span data-ttu-id="a475a-114">Wymusz uruchomienie polecenia bez podaniem dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="a475a-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="a475a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a475a-115">-InputObject</span></span>
<span data-ttu-id="a475a-116">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania kontenera ochrony asr, odpowiadający kontenerowi ochrony do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a475a-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a475a-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a475a-117">-Confirm</span></span>
<span data-ttu-id="a475a-118">Określ, czy jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a475a-118">Specify if confirmation is required.</span></span> <span data-ttu-id="a475a-119">Ustawianie wartości parametru confirm w celu $false w celu pominięcia potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="a475a-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="a475a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a475a-120">-WhatIf</span></span>
<span data-ttu-id="a475a-121">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie wykonane bez wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a475a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="a475a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a475a-122">CommonParameters</span></span>
<span data-ttu-id="a475a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a475a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a475a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a475a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a475a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a475a-125">INPUTS</span></span>

### <span data-ttu-id="a475a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a475a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="a475a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a475a-127">OUTPUTS</span></span>

### <span data-ttu-id="a475a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a475a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a475a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a475a-129">NOTES</span></span>

## <span data-ttu-id="a475a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a475a-130">RELATED LINKS</span></span>

[<span data-ttu-id="a475a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a475a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="a475a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a475a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240259"
---
# <span data-ttu-id="a1fc8-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a1fc8-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a1fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fc8-103">Usuwa określony plan odzyskiwania asr z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="a1fc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1fc8-104">SYNTAX</span></span>

### <span data-ttu-id="a1fc8-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a1fc8-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fc8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a1fc8-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1fc8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="a1fc8-108">Polecenie **cmdlet Remove-AzRecoveryServicesAsrRecoveryPlan** usuwa określony plan odzyskiwania z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="a1fc8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="a1fc8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1fc8-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="a1fc8-111">Rozpoczyna usuwanie określonego planu odzyskiwania i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a1fc8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1fc8-112">PARAMETERS</span></span>

### <span data-ttu-id="a1fc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fc8-113">-DefaultProfile</span></span>
<span data-ttu-id="a1fc8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a1fc8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1fc8-115">-InputObject</span></span>
<span data-ttu-id="a1fc8-116">Obiekt wejściowy do polecenia cmdlet: obiekt planu odzyskiwania asr odpowiadający planowi odzyskiwania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1fc8-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1fc8-117">-Name</span></span>
<span data-ttu-id="a1fc8-118">Określa nazwę planu odzyskiwania, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fc8-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1fc8-119">-Confirm</span></span>
<span data-ttu-id="a1fc8-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1fc8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1fc8-121">-WhatIf</span></span>
<span data-ttu-id="a1fc8-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1fc8-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1fc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fc8-124">CommonParameters</span></span>
<span data-ttu-id="a1fc8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fc8-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1fc8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fc8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1fc8-127">INPUTS</span></span>

### <span data-ttu-id="a1fc8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a1fc8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a1fc8-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1fc8-129">OUTPUTS</span></span>

### <span data-ttu-id="a1fc8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a1fc8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a1fc8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1fc8-131">NOTES</span></span>

## <span data-ttu-id="a1fc8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1fc8-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1fc8-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a1fc8-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a1fc8-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a1fc8-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a1fc8-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a1fc8-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)



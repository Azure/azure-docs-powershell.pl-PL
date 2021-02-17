---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192818"
---
# <span data-ttu-id="bb66e-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bb66e-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="bb66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb66e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb66e-103">Zaktualizuj mapowanie kontenera ochrony przed odzyskiwaniem witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb66e-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="bb66e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb66e-104">SYNTAX</span></span>

### <span data-ttu-id="bb66e-105">AzureToAzureEnableAutoUpdate (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bb66e-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb66e-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bb66e-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb66e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb66e-107">DESCRIPTION</span></span>
<span data-ttu-id="bb66e-108">Polecenie **cmdlet Update-AzRecoveryServicesAsrProtectionContainerMapping** aktualizuje wskazane mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bb66e-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="bb66e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb66e-109">EXAMPLES</span></span>

### <span data-ttu-id="bb66e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb66e-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="bb66e-111">Uruchom operację, aby wyłączyć automatyczną aktualizację dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="bb66e-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="bb66e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb66e-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="bb66e-113">Aby wyłączyć automatyczne aktualizowanie kontenera, rozpocznij operację.</span><span class="sxs-lookup"><span data-stu-id="bb66e-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="bb66e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb66e-114">PARAMETERS</span></span>

### <span data-ttu-id="bb66e-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="bb66e-115">-AutomationAccountId</span></span>
<span data-ttu-id="bb66e-116">Określa wartość automatyzacji accountId używaną do automatycznego udpate.</span><span class="sxs-lookup"><span data-stu-id="bb66e-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bb66e-117">-AzureToAzure</span></span>
<span data-ttu-id="bb66e-118">Określa kontener platformy Azure do usługi Azure Protection.</span><span class="sxs-lookup"><span data-stu-id="bb66e-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb66e-119">-DefaultProfile</span></span>
<span data-ttu-id="bb66e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb66e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb66e-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bb66e-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="bb66e-122">Przełącz parametr, aby wyłączyć automatyczną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="bb66e-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bb66e-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="bb66e-124">Przełącz parametr, aby włączyć automatyczną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="bb66e-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb66e-125">-InputObject</span></span>
<span data-ttu-id="bb66e-126">Obiekt do mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="bb66e-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="bb66e-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb66e-127">-Confirm</span></span>
<span data-ttu-id="bb66e-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb66e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb66e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb66e-129">-WhatIf</span></span>
<span data-ttu-id="bb66e-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb66e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb66e-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb66e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb66e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb66e-132">CommonParameters</span></span>
<span data-ttu-id="bb66e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb66e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb66e-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb66e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb66e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb66e-135">INPUTS</span></span>

### <span data-ttu-id="bb66e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bb66e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="bb66e-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb66e-137">OUTPUTS</span></span>

### <span data-ttu-id="bb66e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bb66e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bb66e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb66e-139">NOTES</span></span>

## <span data-ttu-id="bb66e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb66e-140">RELATED LINKS</span></span>

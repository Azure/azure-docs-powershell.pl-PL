---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951002"
---
# <span data-ttu-id="4692b-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4692b-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="4692b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4692b-102">SYNOPSIS</span></span>
<span data-ttu-id="4692b-103">Zaktualizuj mapowanie kontenera ochrony przed odzyskiwaniem witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4692b-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="4692b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4692b-104">SYNTAX</span></span>

### <span data-ttu-id="4692b-105">AzureToAzureEnableAutoUpdate (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4692b-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4692b-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4692b-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4692b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4692b-107">DESCRIPTION</span></span>
<span data-ttu-id="4692b-108">Polecenie **cmdlet Update-AzRecoveryServicesAsrProtectionContainerMapping** aktualizuje wskazane mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4692b-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="4692b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4692b-109">EXAMPLES</span></span>

### <span data-ttu-id="4692b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4692b-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="4692b-111">Uruchom operację, aby wyłączyć automatyczną aktualizację dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="4692b-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="4692b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4692b-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="4692b-113">Aby wyłączyć automatyczne aktualizowanie kontenera, rozpocznij operację.</span><span class="sxs-lookup"><span data-stu-id="4692b-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="4692b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4692b-114">PARAMETERS</span></span>

### <span data-ttu-id="4692b-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="4692b-115">-AutomationAccountId</span></span>
<span data-ttu-id="4692b-116">Określa wartość automatyzacji accountId używaną do automatycznego udpatowania.</span><span class="sxs-lookup"><span data-stu-id="4692b-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="4692b-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4692b-117">-AzureToAzure</span></span>
<span data-ttu-id="4692b-118">Określa kontener platformy Azure do usługi Azure Protection.</span><span class="sxs-lookup"><span data-stu-id="4692b-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="4692b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4692b-119">-DefaultProfile</span></span>
<span data-ttu-id="4692b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4692b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4692b-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4692b-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="4692b-122">Przełącz parametr, aby wyłączyć automatyczną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="4692b-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="4692b-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4692b-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="4692b-124">Przełącz parametr, aby włączyć automatyczną aktualizację.</span><span class="sxs-lookup"><span data-stu-id="4692b-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="4692b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4692b-125">-InputObject</span></span>
<span data-ttu-id="4692b-126">Obiekt do mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="4692b-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="4692b-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4692b-127">-Confirm</span></span>
<span data-ttu-id="4692b-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4692b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4692b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4692b-129">-WhatIf</span></span>
<span data-ttu-id="4692b-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4692b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4692b-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4692b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4692b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4692b-132">CommonParameters</span></span>
<span data-ttu-id="4692b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4692b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4692b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4692b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4692b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4692b-135">INPUTS</span></span>

### <span data-ttu-id="4692b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4692b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="4692b-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4692b-137">OUTPUTS</span></span>

### <span data-ttu-id="4692b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4692b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4692b-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4692b-139">NOTES</span></span>

## <span data-ttu-id="4692b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4692b-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490769"
---
# <span data-ttu-id="dd9ac-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dd9ac-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="dd9ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9ac-103">Zaktualizuj mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="dd9ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd9ac-104">SYNTAX</span></span>

### <span data-ttu-id="dd9ac-105">AzureToAzureEnableAutoUpdate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd9ac-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9ac-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="dd9ac-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd9ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd9ac-107">DESCRIPTION</span></span>
<span data-ttu-id="dd9ac-108">Polecenie cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** aktualizuje określone mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="dd9ac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd9ac-109">EXAMPLES</span></span>

### <span data-ttu-id="dd9ac-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd9ac-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="dd9ac-111">Rozpocznij operację wyłączania automatycznej aktualizacji kontenera.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="dd9ac-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dd9ac-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="dd9ac-113">Rozpocznij operację wyłączania Włącz automatyczne aktualizowanie kontenera.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="dd9ac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd9ac-114">PARAMETERS</span></span>

### <span data-ttu-id="dd9ac-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="dd9ac-115">-AutomationAccountId</span></span>
<span data-ttu-id="dd9ac-116">Określa identyfikator accountId służący do automatycznego udpate.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="dd9ac-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="dd9ac-117">-AzureToAzure</span></span>
<span data-ttu-id="dd9ac-118">Określa kontener ochrony platformy Azure na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="dd9ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9ac-119">-DefaultProfile</span></span>
<span data-ttu-id="dd9ac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9ac-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="dd9ac-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="dd9ac-122">Parametr Switch umożliwiający wyłączenie automatycznej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="dd9ac-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="dd9ac-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="dd9ac-124">Parametr Switch umożliwiający włączenie automatycznej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="dd9ac-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd9ac-125">-InputObject</span></span>
<span data-ttu-id="dd9ac-126">Obiekt mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="dd9ac-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd9ac-127">-Confirm</span></span>
<span data-ttu-id="dd9ac-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9ac-129">-WhatIf</span></span>
<span data-ttu-id="dd9ac-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd9ac-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9ac-132">CommonParameters</span></span>
<span data-ttu-id="dd9ac-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd9ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9ac-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd9ac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9ac-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd9ac-135">INPUTS</span></span>

### <span data-ttu-id="dd9ac-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dd9ac-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="dd9ac-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd9ac-137">OUTPUTS</span></span>

### <span data-ttu-id="dd9ac-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dd9ac-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dd9ac-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd9ac-139">NOTES</span></span>

## <span data-ttu-id="dd9ac-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd9ac-140">RELATED LINKS</span></span>

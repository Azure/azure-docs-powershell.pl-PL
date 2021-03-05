---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 24c5f3b93b2be446eed4e5b81e1e69bf2116aa8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961969"
---
# <span data-ttu-id="4ec28-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ec28-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4ec28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec28-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec28-103">Usuwa konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="4ec28-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ec28-104">SYNTAX</span></span>

### <span data-ttu-id="4ec28-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4ec28-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ec28-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec28-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec28-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec28-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ec28-108">DESCRIPTION</span></span>
<span data-ttu-id="4ec28-109">Polecenie **cmdlet Remove-AzIntegrationAccountBatchConfiguration** usuwa konfigurację partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="4ec28-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ec28-110">EXAMPLES</span></span>

### <span data-ttu-id="4ec28-111">Przykład 1. Usuwanie konfiguracji partii według parametrów</span><span class="sxs-lookup"><span data-stu-id="4ec28-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="4ec28-112">Usuwa konfigurację partii o nazwie "sampleBatchConfig" znajdującą się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="4ec28-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="4ec28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ec28-113">PARAMETERS</span></span>

### <span data-ttu-id="4ec28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec28-114">-DefaultProfile</span></span>
<span data-ttu-id="4ec28-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec28-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ec28-116">-InputObject</span></span>
<span data-ttu-id="4ec28-117">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec28-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ec28-118">-Name</span></span>
<span data-ttu-id="4ec28-119">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec28-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4ec28-120">-ParentName</span></span>
<span data-ttu-id="4ec28-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec28-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ec28-122">-PassThru</span></span>
<span data-ttu-id="4ec28-123">Zwracanie, czy polecenie zostało pomyślnie lub nie.</span><span class="sxs-lookup"><span data-stu-id="4ec28-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="4ec28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec28-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ec28-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ec28-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec28-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec28-126">-ResourceId</span></span>
<span data-ttu-id="4ec28-127">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4ec28-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec28-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ec28-128">-Confirm</span></span>
<span data-ttu-id="4ec28-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ec28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec28-130">-WhatIf</span></span>
<span data-ttu-id="4ec28-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ec28-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ec28-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ec28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec28-133">CommonParameters</span></span>
<span data-ttu-id="4ec28-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec28-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec28-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ec28-136">INPUTS</span></span>

### <span data-ttu-id="4ec28-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ec28-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="4ec28-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec28-138">System.String</span></span>

## <span data-ttu-id="4ec28-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ec28-139">OUTPUTS</span></span>

### <span data-ttu-id="4ec28-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ec28-140">System.Boolean</span></span>

## <span data-ttu-id="4ec28-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ec28-141">NOTES</span></span>

## <span data-ttu-id="4ec28-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ec28-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185194"
---
# <span data-ttu-id="37877-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37877-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="37877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37877-102">SYNOPSIS</span></span>
<span data-ttu-id="37877-103">Usuwa konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="37877-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37877-104">SYNTAX</span></span>

### <span data-ttu-id="37877-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="37877-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37877-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37877-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37877-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="37877-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37877-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="37877-108">DESCRIPTION</span></span>
<span data-ttu-id="37877-109">Polecenie **cmdlet Remove-AzIntegrationAccountBatchConfiguration** usuwa konfigurację partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="37877-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37877-110">EXAMPLES</span></span>

### <span data-ttu-id="37877-111">Przykład 1. Usuwanie konfiguracji partii według parametrów</span><span class="sxs-lookup"><span data-stu-id="37877-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="37877-112">Usuwa konfigurację partii o nazwie "sampleBatchConfig" znajdującą się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="37877-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="37877-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37877-113">PARAMETERS</span></span>

### <span data-ttu-id="37877-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37877-114">-DefaultProfile</span></span>
<span data-ttu-id="37877-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37877-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37877-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37877-116">-InputObject</span></span>
<span data-ttu-id="37877-117">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="37877-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37877-118">-Name</span></span>
<span data-ttu-id="37877-119">Nazwa partii partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="37877-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="37877-120">-ParentName</span></span>
<span data-ttu-id="37877-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-121">The integration account name.</span></span>

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

### <span data-ttu-id="37877-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37877-122">-PassThru</span></span>
<span data-ttu-id="37877-123">Zwracanie, czy polecenie zostało pomyślnie lub nie.</span><span class="sxs-lookup"><span data-stu-id="37877-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="37877-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37877-124">-ResourceGroupName</span></span>
<span data-ttu-id="37877-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37877-125">The resource group name.</span></span>

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

### <span data-ttu-id="37877-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37877-126">-ResourceId</span></span>
<span data-ttu-id="37877-127">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="37877-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="37877-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37877-128">-Confirm</span></span>
<span data-ttu-id="37877-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37877-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37877-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37877-130">-WhatIf</span></span>
<span data-ttu-id="37877-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37877-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37877-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37877-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37877-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37877-133">CommonParameters</span></span>
<span data-ttu-id="37877-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37877-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37877-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37877-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37877-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37877-136">INPUTS</span></span>

### <span data-ttu-id="37877-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37877-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="37877-138">System.String</span><span class="sxs-lookup"><span data-stu-id="37877-138">System.String</span></span>

## <span data-ttu-id="37877-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37877-139">OUTPUTS</span></span>

### <span data-ttu-id="37877-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37877-140">System.Boolean</span></span>

## <span data-ttu-id="37877-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37877-141">NOTES</span></span>

## <span data-ttu-id="37877-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37877-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: e2c4f3f399bd4bcd472ae04c6ca2234c2d2b26d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704999"
---
# <span data-ttu-id="5e8a7-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e8a7-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="5e8a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8a7-103">Usuwa konfigurację partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="5e8a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e8a7-104">SYNTAX</span></span>

### <span data-ttu-id="5e8a7-105">ByIntegrationAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e8a7-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e8a7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e8a7-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e8a7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a7-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e8a7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e8a7-108">DESCRIPTION</span></span>
<span data-ttu-id="5e8a7-109">Polecenie cmdlet **Remove-AzIntegrationAccountBatchConfiguration** umożliwia usunięcie konfiguracji partii z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="5e8a7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e8a7-110">EXAMPLES</span></span>

### <span data-ttu-id="5e8a7-111">Przykład 1: Usuwanie konfiguracji wsadowej według parametrów</span><span class="sxs-lookup"><span data-stu-id="5e8a7-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="5e8a7-112">Usuwa konfigurację wsadową o nazwie "sampleBatchConfig" znajdującą się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="5e8a7-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="5e8a7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e8a7-113">PARAMETERS</span></span>

### <span data-ttu-id="5e8a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8a7-114">-DefaultProfile</span></span>
<span data-ttu-id="5e8a7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8a7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e8a7-116">-InputObject</span></span>
<span data-ttu-id="5e8a7-117">Konfiguracja partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="5e8a7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e8a7-118">-Name</span></span>
<span data-ttu-id="5e8a7-119">Nazwa konfiguracji wsadowej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="5e8a7-120">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="5e8a7-120">-ParentName</span></span>
<span data-ttu-id="5e8a7-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-121">The integration account name.</span></span>

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

### <span data-ttu-id="5e8a7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e8a7-122">-PassThru</span></span>
<span data-ttu-id="5e8a7-123">Zwraca, czy polecenie zostało wykonane prawidłowo, czy nie.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="5e8a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e8a7-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-125">The resource group name.</span></span>

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

### <span data-ttu-id="5e8a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a7-126">-ResourceId</span></span>
<span data-ttu-id="5e8a7-127">Identyfikator zasobu konfiguracji partii konta integracji.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="5e8a7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e8a7-128">-Confirm</span></span>
<span data-ttu-id="5e8a7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e8a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e8a7-130">-WhatIf</span></span>
<span data-ttu-id="5e8a7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e8a7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e8a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8a7-133">CommonParameters</span></span>
<span data-ttu-id="5e8a7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8a7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e8a7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8a7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e8a7-136">INPUTS</span></span>

### <span data-ttu-id="5e8a7-137">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e8a7-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="5e8a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5e8a7-138">System.String</span></span>

## <span data-ttu-id="5e8a7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e8a7-139">OUTPUTS</span></span>

### <span data-ttu-id="5e8a7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e8a7-140">System.Boolean</span></span>

## <span data-ttu-id="5e8a7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e8a7-141">NOTES</span></span>

## <span data-ttu-id="5e8a7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e8a7-142">RELATED LINKS</span></span>

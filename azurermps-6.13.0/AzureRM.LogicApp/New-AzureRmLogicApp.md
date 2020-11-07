---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 0cc84438e67fd6fb57f5157825b21b3213beb8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719111"
---
# <span data-ttu-id="9f22e-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9f22e-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="9f22e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f22e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f22e-103">Tworzy aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f22e-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f22e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f22e-104">SYNTAX</span></span>

### <span data-ttu-id="9f22e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f22e-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f22e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f22e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f22e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9f22e-107">DESCRIPTION</span></span>
<span data-ttu-id="9f22e-108">Polecenie cmdlet **New-AzureRmLogicApp** tworzy aplikację logiczną za pomocą funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="9f22e-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="9f22e-109">Aplikacja logiczna to kolekcja akcji lub wyzwalaczy zdefiniowana w definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="9f22e-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="9f22e-110">To polecenie cmdlet zwraca obiekt **przepływu pracy** .</span><span class="sxs-lookup"><span data-stu-id="9f22e-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="9f22e-111">Możesz utworzyć aplikację logiczną, określając nazwę, lokalizację, definicję aplikacji logicznej, grupę zasobów i plan.</span><span class="sxs-lookup"><span data-stu-id="9f22e-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="9f22e-112">Definicje i parametry aplikacji logiki są sformatowane w notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9f22e-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="9f22e-113">W celu określenia definicji i parametrów można użyć aplikacji logicznej jako szablonu.</span><span class="sxs-lookup"><span data-stu-id="9f22e-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="9f22e-114">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="9f22e-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9f22e-115">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9f22e-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9f22e-116">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="9f22e-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9f22e-117">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="9f22e-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="9f22e-118">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="9f22e-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="9f22e-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f22e-119">EXAMPLES</span></span>

### <span data-ttu-id="9f22e-120">Przykład 1: Tworzenie aplikacji logicznej przy użyciu ścieżek plików definicji i parametrów</span><span class="sxs-lookup"><span data-stu-id="9f22e-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="9f22e-121">To polecenie tworzy aplikację logiczną w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f22e-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="9f22e-122">Aplikacja logiczna obejmuje definicje i parametry określone przez ścieżki plików.</span><span class="sxs-lookup"><span data-stu-id="9f22e-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="9f22e-123">Przykład 2: Tworzenie aplikacji logicznej przy użyciu obiektów definicji i parametrów</span><span class="sxs-lookup"><span data-stu-id="9f22e-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="9f22e-124">To polecenie tworzy aplikację logiczną w określonej grupie zasobów Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f22e-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="9f22e-125">Przykład 3: Tworzenie aplikacji logicznej za pomocą potoku w celu określenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9f22e-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="9f22e-126">To polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu polecenia cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9f22e-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="9f22e-127">Polecenie przekazuje tę grupę zasobów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9f22e-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f22e-128">Bieżące polecenie cmdlet powoduje utworzenie aplikacji logicznej w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f22e-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="9f22e-129">Aplikacja logiczna obejmuje definicje i parametry określone przez ścieżki plików.</span><span class="sxs-lookup"><span data-stu-id="9f22e-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="9f22e-130">Przykład 4: Tworzenie aplikacji logicznej na podstawie istniejącej aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="9f22e-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="9f22e-131">Pierwsze polecenie uzyskuje aplikację logiczną o nazwie LogicApp03 przy użyciu polecenia cmdlet Get-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="9f22e-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="9f22e-132">Polecenie zapisuje aplikację logiczną w zmiennej $Workflow.</span><span class="sxs-lookup"><span data-stu-id="9f22e-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="9f22e-133">Drugie polecenie tworzy nową aplikację logiczną, która używa definicji i parametrów aplikacji logicznej przechowywanej w $Workflow.</span><span class="sxs-lookup"><span data-stu-id="9f22e-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="9f22e-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f22e-134">PARAMETERS</span></span>

### <span data-ttu-id="9f22e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f22e-135">-DefaultProfile</span></span>
<span data-ttu-id="9f22e-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f22e-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-137">-Definicja</span><span class="sxs-lookup"><span data-stu-id="9f22e-137">-Definition</span></span>
<span data-ttu-id="9f22e-138">Określa definicję aplikacji logicznej jako obiekt lub ciąg w formacie Notataion obiektu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="9f22e-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="9f22e-139">-DefinitionFilePath</span></span>
<span data-ttu-id="9f22e-140">Określa definicję aplikacji logicznej jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="9f22e-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="9f22e-141">-IntegrationAccountId</span></span>
<span data-ttu-id="9f22e-142">Określa identyfikator konta integracyjnego dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="9f22e-142">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9f22e-143">-Location</span></span>
<span data-ttu-id="9f22e-144">Określa lokalizację aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="9f22e-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="9f22e-145">Wprowadź lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia USA lub południowo-zachodni.</span><span class="sxs-lookup"><span data-stu-id="9f22e-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="9f22e-146">Aplikację logiczną można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f22e-146">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f22e-147">-Name</span></span>
<span data-ttu-id="9f22e-148">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="9f22e-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="9f22e-149">-ParameterFilePath</span></span>
<span data-ttu-id="9f22e-150">Określa ścieżkę pliku parametrów w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="9f22e-150">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-151">— Parametry</span><span class="sxs-lookup"><span data-stu-id="9f22e-151">-Parameters</span></span>
<span data-ttu-id="9f22e-152">Określa obiekt kolekcji Parameters dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="9f22e-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="9f22e-153">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="9f22e-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f22e-154">-ResourceGroupName</span></span>
<span data-ttu-id="9f22e-155">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9f22e-155">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-156">-State</span><span class="sxs-lookup"><span data-stu-id="9f22e-156">-State</span></span>
<span data-ttu-id="9f22e-157">Określa stan aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="9f22e-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="9f22e-158">Dopuszczalne wartości tego parametru są następujące: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="9f22e-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f22e-159">-Confirm</span></span>
<span data-ttu-id="9f22e-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f22e-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f22e-161">-WhatIf</span></span>
<span data-ttu-id="9f22e-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f22e-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f22e-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f22e-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f22e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f22e-164">CommonParameters</span></span>
<span data-ttu-id="9f22e-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f22e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f22e-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f22e-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f22e-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f22e-167">INPUTS</span></span>

### <span data-ttu-id="9f22e-168">System. String</span><span class="sxs-lookup"><span data-stu-id="9f22e-168">System.String</span></span>

## <span data-ttu-id="9f22e-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f22e-169">OUTPUTS</span></span>

### <span data-ttu-id="9f22e-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f22e-170">System.Object</span></span>

## <span data-ttu-id="9f22e-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f22e-171">NOTES</span></span>

## <span data-ttu-id="9f22e-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f22e-172">RELATED LINKS</span></span>

[<span data-ttu-id="9f22e-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9f22e-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="9f22e-174">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9f22e-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="9f22e-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9f22e-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="9f22e-176">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="9f22e-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



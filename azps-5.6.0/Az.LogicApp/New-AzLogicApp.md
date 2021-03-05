---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 98fb733f661d4d1c5a6c50ce472005763584a72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968954"
---
# <span data-ttu-id="1393d-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1393d-101">New-AzLogicApp</span></span>

## <span data-ttu-id="1393d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1393d-102">SYNOPSIS</span></span>
<span data-ttu-id="1393d-103">Tworzy aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1393d-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="1393d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1393d-104">SYNTAX</span></span>

### <span data-ttu-id="1393d-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1393d-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1393d-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1393d-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1393d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1393d-107">DESCRIPTION</span></span>
<span data-ttu-id="1393d-108">Polecenie **cmdlet New-AzLogicApp** tworzy aplikację logiki przy użyciu funkcji aplikacje logic.</span><span class="sxs-lookup"><span data-stu-id="1393d-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="1393d-109">Aplikacja logiki to zbiór akcji lub wyzwalaczy zdefiniowanych w definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="1393d-110">To polecenie cmdlet zwraca obiekt **przepływu** pracy.</span><span class="sxs-lookup"><span data-stu-id="1393d-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="1393d-111">Możesz utworzyć aplikację logiki, określając nazwę, lokalizację, definicję aplikacji logiki, grupę zasobów i plan.</span><span class="sxs-lookup"><span data-stu-id="1393d-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="1393d-112">Definicja i parametry aplikacji logiki są sformatowane w notacji obiektów JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="1393d-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="1393d-113">Jako szablonu definicji i parametrów można użyć aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="1393d-114">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="1393d-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1393d-115">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1393d-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1393d-116">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="1393d-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1393d-117">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="1393d-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="1393d-118">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="1393d-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="1393d-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1393d-119">EXAMPLES</span></span>

### <span data-ttu-id="1393d-120">Przykład 1. Tworzenie aplikacji logiki przy użyciu ścieżek plików definicji i parametrów</span><span class="sxs-lookup"><span data-stu-id="1393d-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="1393d-121">To polecenie umożliwia utworzenie aplikacji logiki w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1393d-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="1393d-122">Aplikacja logiki zawiera definicję i parametry określone przez ścieżki plików.</span><span class="sxs-lookup"><span data-stu-id="1393d-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="1393d-123">Przykład 2. Tworzenie aplikacji logiki przy użyciu obiektów definicji i parametrów</span><span class="sxs-lookup"><span data-stu-id="1393d-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="1393d-124">To polecenie tworzy aplikację logiki w grupie zasobów określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1393d-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="1393d-125">Przykład 3. Tworzenie aplikacji logiki przy użyciu potoku w celu określenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1393d-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="1393d-126">To polecenie pobiera grupę zasobów o nazwie ResourceGroup11 przy użyciu Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1393d-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1393d-127">Polecenie przekazuje grupę zasobów do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1393d-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1393d-128">Bieżące polecenie cmdlet tworzy aplikację logiczną w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1393d-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="1393d-129">Aplikacja logiki zawiera definicję i parametry określone przez ścieżki plików.</span><span class="sxs-lookup"><span data-stu-id="1393d-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="1393d-130">Przykład 4. Tworzenie aplikacji logiki na podstawie istniejącej aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="1393d-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="1393d-131">Pierwsze polecenie pobiera aplikację logiki o nazwie LogicApp03 za pomocą Get-AzLogicApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1393d-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="1393d-132">Polecenie zapisuje aplikację logiki w $Workflow zmienną.</span><span class="sxs-lookup"><span data-stu-id="1393d-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="1393d-133">Drugie polecenie tworzy nową aplikację logiki, która korzysta z definicji i parametrów aplikacji logiki przechowywanej w $Workflow.</span><span class="sxs-lookup"><span data-stu-id="1393d-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="1393d-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1393d-134">PARAMETERS</span></span>

### <span data-ttu-id="1393d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1393d-135">-DefaultProfile</span></span>
<span data-ttu-id="1393d-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1393d-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1393d-137">—Definicja</span><span class="sxs-lookup"><span data-stu-id="1393d-137">-Definition</span></span>
<span data-ttu-id="1393d-138">Określa definicję aplikacji logiki jako obiekt lub ciąg w formacie JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="1393d-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="1393d-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="1393d-139">-DefinitionFilePath</span></span>
<span data-ttu-id="1393d-140">Określa definicję aplikacji logiki jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="1393d-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="1393d-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="1393d-141">-IntegrationAccountId</span></span>
<span data-ttu-id="1393d-142">Określa identyfikator konta integracji dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="1393d-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1393d-143">-Location</span></span>
<span data-ttu-id="1393d-144">Określa lokalizację aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="1393d-145">Wprowadź lokalizację centrum danych platformy Azure, taką jak Stany Zjednoczone i Azja Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="1393d-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="1393d-146">Aplikację logiki można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1393d-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="1393d-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1393d-147">-Name</span></span>
<span data-ttu-id="1393d-148">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="1393d-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="1393d-149">-ParameterFilePath</span></span>
<span data-ttu-id="1393d-150">Określa ścieżkę pliku sformatowanych parametrów JSON.</span><span class="sxs-lookup"><span data-stu-id="1393d-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="1393d-151">— Parametry</span><span class="sxs-lookup"><span data-stu-id="1393d-151">-Parameters</span></span>
<span data-ttu-id="1393d-152">Określa obiekt kolekcji parametrów dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="1393d-153">Określ tabelę skrótu, słownik \<string\> lub \<string, WorkflowParameter\> słownik.</span><span class="sxs-lookup"><span data-stu-id="1393d-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="1393d-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1393d-154">-ResourceGroupName</span></span>
<span data-ttu-id="1393d-155">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1393d-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1393d-156">— województwo</span><span class="sxs-lookup"><span data-stu-id="1393d-156">-State</span></span>
<span data-ttu-id="1393d-157">Określa stan aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="1393d-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="1393d-158">Dopuszczalne wartości dla tego parametru to: Włączone i Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="1393d-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="1393d-159">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1393d-159">-Confirm</span></span>
<span data-ttu-id="1393d-160">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1393d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1393d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1393d-161">-WhatIf</span></span>
<span data-ttu-id="1393d-162">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1393d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1393d-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1393d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1393d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1393d-164">CommonParameters</span></span>
<span data-ttu-id="1393d-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1393d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1393d-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1393d-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1393d-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1393d-167">INPUTS</span></span>

### <span data-ttu-id="1393d-168">System.String</span><span class="sxs-lookup"><span data-stu-id="1393d-168">System.String</span></span>

## <span data-ttu-id="1393d-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1393d-169">OUTPUTS</span></span>

### <span data-ttu-id="1393d-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="1393d-170">System.Object</span></span>

## <span data-ttu-id="1393d-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1393d-171">NOTES</span></span>

## <span data-ttu-id="1393d-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1393d-172">RELATED LINKS</span></span>

[<span data-ttu-id="1393d-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1393d-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="1393d-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1393d-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="1393d-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1393d-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="1393d-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1393d-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



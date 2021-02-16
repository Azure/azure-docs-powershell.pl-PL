---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194187"
---
# <span data-ttu-id="66b5e-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66b5e-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="66b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="66b5e-103">Modyfikuje aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="66b5e-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="66b5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66b5e-104">SYNTAX</span></span>

### <span data-ttu-id="66b5e-105">Zużycie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="66b5e-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66b5e-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="66b5e-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66b5e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="66b5e-107">DESCRIPTION</span></span>
<span data-ttu-id="66b5e-108">Polecenie **cmdlet Set-AzLogicApp** modyfikuje aplikację logiki przy użyciu funkcji aplikacje logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="66b5e-109">Aplikacja logiczna to zbiór akcji lub wyzwalaczy zdefiniowanych w definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="66b5e-110">To polecenie cmdlet zwraca obiekt **przepływu** pracy.</span><span class="sxs-lookup"><span data-stu-id="66b5e-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="66b5e-111">Aplikację logiki można zmodyfikować, określając nazwę, lokalizację, definicję aplikacji logiki, grupę zasobów i plan.</span><span class="sxs-lookup"><span data-stu-id="66b5e-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="66b5e-112">Definicja i parametry aplikacji logiki są sformatowane w notacji obiektów JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="66b5e-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="66b5e-113">Jako szablonu definicji i parametrów można użyć aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="66b5e-114">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="66b5e-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="66b5e-115">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="66b5e-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="66b5e-116">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="66b5e-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="66b5e-117">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="66b5e-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="66b5e-118">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="66b5e-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="66b5e-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66b5e-119">EXAMPLES</span></span>

### <span data-ttu-id="66b5e-120">Przykład 1. Modyfikowanie aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="66b5e-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="66b5e-121">To polecenie modyfikuje aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="66b5e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66b5e-122">PARAMETERS</span></span>

### <span data-ttu-id="66b5e-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="66b5e-123">-AppServicePlan</span></span>
<span data-ttu-id="66b5e-124">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="66b5e-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b5e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b5e-125">-DefaultProfile</span></span>
<span data-ttu-id="66b5e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="66b5e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66b5e-127">—Definicja</span><span class="sxs-lookup"><span data-stu-id="66b5e-127">-Definition</span></span>
<span data-ttu-id="66b5e-128">Określa definicję aplikacji logiki jako obiektu lub ciągu w formacie JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="66b5e-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="66b5e-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="66b5e-129">-DefinitionFilePath</span></span>
<span data-ttu-id="66b5e-130">Określa definicję aplikacji logiki jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="66b5e-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="66b5e-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="66b5e-131">-Force</span></span>
<span data-ttu-id="66b5e-132">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="66b5e-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66b5e-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="66b5e-133">-IntegrationAccountId</span></span>
<span data-ttu-id="66b5e-134">Określa identyfikator konta integracji dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="66b5e-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66b5e-135">-Name</span></span>
<span data-ttu-id="66b5e-136">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="66b5e-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="66b5e-137">-ParameterFilePath</span></span>
<span data-ttu-id="66b5e-138">Określa ścieżkę pliku parametrów sformatowanych jako JSON.</span><span class="sxs-lookup"><span data-stu-id="66b5e-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="66b5e-139">— Parametry</span><span class="sxs-lookup"><span data-stu-id="66b5e-139">-Parameters</span></span>
<span data-ttu-id="66b5e-140">Określa obiekt kolekcji parametrów dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="66b5e-141">Określ tabelę \<string\> skrótów, słownik lub \<string, WorkflowParameter\> słownik.</span><span class="sxs-lookup"><span data-stu-id="66b5e-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="66b5e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b5e-142">-ResourceGroupName</span></span>
<span data-ttu-id="66b5e-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66b5e-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="66b5e-144">— województwo</span><span class="sxs-lookup"><span data-stu-id="66b5e-144">-State</span></span>
<span data-ttu-id="66b5e-145">Określa stan aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="66b5e-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="66b5e-146">Dopuszczalne wartości dla tego parametru to: Włączone i Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="66b5e-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="66b5e-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="66b5e-147">-UseConsumptionModel</span></span>
<span data-ttu-id="66b5e-148">Wskazuje, że w rozliczeniach aplikacji logicznych jest oparty na modelu zużycia.</span><span class="sxs-lookup"><span data-stu-id="66b5e-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b5e-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="66b5e-149">-Confirm</span></span>
<span data-ttu-id="66b5e-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="66b5e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b5e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b5e-151">-WhatIf</span></span>
<span data-ttu-id="66b5e-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b5e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b5e-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="66b5e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b5e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b5e-154">CommonParameters</span></span>
<span data-ttu-id="66b5e-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b5e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b5e-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b5e-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b5e-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66b5e-157">INPUTS</span></span>

### <span data-ttu-id="66b5e-158">System.String</span><span class="sxs-lookup"><span data-stu-id="66b5e-158">System.String</span></span>

## <span data-ttu-id="66b5e-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66b5e-159">OUTPUTS</span></span>

### <span data-ttu-id="66b5e-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="66b5e-160">System.Object</span></span>

## <span data-ttu-id="66b5e-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66b5e-161">NOTES</span></span>

## <span data-ttu-id="66b5e-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66b5e-162">RELATED LINKS</span></span>

[<span data-ttu-id="66b5e-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66b5e-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="66b5e-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66b5e-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="66b5e-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66b5e-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="66b5e-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="66b5e-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



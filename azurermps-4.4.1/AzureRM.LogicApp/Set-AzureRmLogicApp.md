---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554351"
---
# <span data-ttu-id="098e5-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="098e5-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="098e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="098e5-102">SYNOPSIS</span></span>
<span data-ttu-id="098e5-103">Modyfikuje aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="098e5-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="098e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="098e5-104">SYNTAX</span></span>

### <span data-ttu-id="098e5-105">Zużycie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="098e5-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="098e5-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="098e5-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="098e5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="098e5-107">DESCRIPTION</span></span>
<span data-ttu-id="098e5-108">Polecenie cmdlet **Set-AzureRmLogicApp** modyfikuje aplikację logiczną za pomocą funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="098e5-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="098e5-109">Aplikacja logiczna to kolekcja akcji lub wyzwalaczy zdefiniowana w definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="098e5-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="098e5-110">To polecenie cmdlet zwraca obiekt **przepływu pracy** .</span><span class="sxs-lookup"><span data-stu-id="098e5-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="098e5-111">Możesz zmodyfikować aplikację logiczną, określając nazwę, lokalizację, definicję aplikacji logicznej, grupę zasobów i plan.</span><span class="sxs-lookup"><span data-stu-id="098e5-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="098e5-112">Definicje i parametry aplikacji logiki są sformatowane w notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="098e5-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="098e5-113">W celu określenia definicji i parametrów można użyć aplikacji logicznej jako szablonu.</span><span class="sxs-lookup"><span data-stu-id="098e5-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="098e5-114">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="098e5-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="098e5-115">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="098e5-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="098e5-116">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="098e5-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="098e5-117">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="098e5-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="098e5-118">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="098e5-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="098e5-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="098e5-119">EXAMPLES</span></span>

### <span data-ttu-id="098e5-120">Przykład 1. Zmodyfikuj aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="098e5-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="098e5-121">To polecenie modyfikuje aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="098e5-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="098e5-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="098e5-122">PARAMETERS</span></span>

### <span data-ttu-id="098e5-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="098e5-123">-AppServicePlan</span></span>
<span data-ttu-id="098e5-124">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="098e5-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="098e5-125">-Definicja</span><span class="sxs-lookup"><span data-stu-id="098e5-125">-Definition</span></span>
<span data-ttu-id="098e5-126">Określa definicję aplikacji logicznej jako obiektu lub ciągu w formacie notacji kodu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="098e5-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="098e5-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="098e5-127">-DefinitionFilePath</span></span>
<span data-ttu-id="098e5-128">Określa definicję aplikacji logicznej jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="098e5-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="098e5-129">-Force</span><span class="sxs-lookup"><span data-stu-id="098e5-129">-Force</span></span>
<span data-ttu-id="098e5-130">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="098e5-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="098e5-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="098e5-131">-IntegrationAccountId</span></span>
<span data-ttu-id="098e5-132">Określa identyfikator konta integracyjnego dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="098e5-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="098e5-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="098e5-133">-Name</span></span>
<span data-ttu-id="098e5-134">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="098e5-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="098e5-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="098e5-135">-ParameterFilePath</span></span>
<span data-ttu-id="098e5-136">Określa ścieżkę pliku parametrów w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="098e5-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="098e5-137">— Parametry</span><span class="sxs-lookup"><span data-stu-id="098e5-137">-Parameters</span></span>
<span data-ttu-id="098e5-138">Określa obiekt kolekcji Parameters dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="098e5-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="098e5-139">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="098e5-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="098e5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098e5-140">-ResourceGroupName</span></span>
<span data-ttu-id="098e5-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="098e5-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="098e5-142">-State</span><span class="sxs-lookup"><span data-stu-id="098e5-142">-State</span></span>
<span data-ttu-id="098e5-143">Określa stan aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="098e5-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="098e5-144">Dopuszczalne wartości tego parametru są następujące: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="098e5-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="098e5-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="098e5-145">-UseConsumptionModel</span></span>
<span data-ttu-id="098e5-146">Wskazuje, że rozliczenia aplikacji logiki korzysta z modelu opartego na zużyciu.</span><span class="sxs-lookup"><span data-stu-id="098e5-146">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="098e5-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="098e5-147">-Confirm</span></span>
<span data-ttu-id="098e5-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098e5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098e5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098e5-149">-WhatIf</span></span>
<span data-ttu-id="098e5-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098e5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098e5-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="098e5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098e5-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098e5-152">-DefaultProfile</span></span>
<span data-ttu-id="098e5-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="098e5-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098e5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098e5-154">CommonParameters</span></span>
<span data-ttu-id="098e5-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098e5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098e5-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="098e5-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098e5-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="098e5-157">INPUTS</span></span>

## <span data-ttu-id="098e5-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="098e5-158">OUTPUTS</span></span>

### <span data-ttu-id="098e5-159">Microsoft. Azure. Management. Logic. models. Workflow</span><span class="sxs-lookup"><span data-stu-id="098e5-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="098e5-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="098e5-160">NOTES</span></span>

## <span data-ttu-id="098e5-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="098e5-161">RELATED LINKS</span></span>

[<span data-ttu-id="098e5-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="098e5-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="098e5-163">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="098e5-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="098e5-164">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="098e5-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="098e5-165">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="098e5-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



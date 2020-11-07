---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: 8fc0a244e893c370d157429d284d7c1790b8a1af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718833"
---
# <span data-ttu-id="afb4f-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="afb4f-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="afb4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="afb4f-103">Modyfikuje aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="afb4f-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afb4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afb4f-104">SYNTAX</span></span>

### <span data-ttu-id="afb4f-105">Zużycie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="afb4f-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb4f-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="afb4f-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="afb4f-107">DESCRIPTION</span></span>
<span data-ttu-id="afb4f-108">Polecenie cmdlet **Set-AzureRmLogicApp** modyfikuje aplikację logiczną za pomocą funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="afb4f-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="afb4f-109">Aplikacja logiczna to kolekcja akcji lub wyzwalaczy zdefiniowana w definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="afb4f-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="afb4f-110">To polecenie cmdlet zwraca obiekt **przepływu pracy** .</span><span class="sxs-lookup"><span data-stu-id="afb4f-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="afb4f-111">Możesz zmodyfikować aplikację logiczną, określając nazwę, lokalizację, definicję aplikacji logicznej, grupę zasobów i plan.</span><span class="sxs-lookup"><span data-stu-id="afb4f-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="afb4f-112">Definicje i parametry aplikacji logiki są sformatowane w notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="afb4f-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="afb4f-113">W celu określenia definicji i parametrów można użyć aplikacji logicznej jako szablonu.</span><span class="sxs-lookup"><span data-stu-id="afb4f-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="afb4f-114">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="afb4f-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="afb4f-115">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="afb4f-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="afb4f-116">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="afb4f-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="afb4f-117">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="afb4f-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="afb4f-118">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="afb4f-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="afb4f-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afb4f-119">EXAMPLES</span></span>

### <span data-ttu-id="afb4f-120">Przykład 1. Zmodyfikuj aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="afb4f-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="afb4f-121">To polecenie modyfikuje aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="afb4f-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="afb4f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afb4f-122">PARAMETERS</span></span>

### <span data-ttu-id="afb4f-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="afb4f-123">-AppServicePlan</span></span>
<span data-ttu-id="afb4f-124">Określa nazwę planu.</span><span class="sxs-lookup"><span data-stu-id="afb4f-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="afb4f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb4f-125">-DefaultProfile</span></span>
<span data-ttu-id="afb4f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="afb4f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afb4f-127">-Definicja</span><span class="sxs-lookup"><span data-stu-id="afb4f-127">-Definition</span></span>
<span data-ttu-id="afb4f-128">Określa definicję aplikacji logicznej jako obiektu lub ciągu w formacie notacji kodu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="afb4f-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="afb4f-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="afb4f-129">-DefinitionFilePath</span></span>
<span data-ttu-id="afb4f-130">Określa definicję aplikacji logicznej jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="afb4f-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="afb4f-131">-Force</span><span class="sxs-lookup"><span data-stu-id="afb4f-131">-Force</span></span>
<span data-ttu-id="afb4f-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="afb4f-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afb4f-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="afb4f-133">-IntegrationAccountId</span></span>
<span data-ttu-id="afb4f-134">Określa identyfikator konta integracyjnego dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="afb4f-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="afb4f-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afb4f-135">-Name</span></span>
<span data-ttu-id="afb4f-136">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="afb4f-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="afb4f-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="afb4f-137">-ParameterFilePath</span></span>
<span data-ttu-id="afb4f-138">Określa ścieżkę pliku parametrów w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="afb4f-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="afb4f-139">— Parametry</span><span class="sxs-lookup"><span data-stu-id="afb4f-139">-Parameters</span></span>
<span data-ttu-id="afb4f-140">Określa obiekt kolekcji Parameters dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="afb4f-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="afb4f-141">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="afb4f-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="afb4f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb4f-142">-ResourceGroupName</span></span>
<span data-ttu-id="afb4f-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="afb4f-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="afb4f-144">-State</span><span class="sxs-lookup"><span data-stu-id="afb4f-144">-State</span></span>
<span data-ttu-id="afb4f-145">Określa stan aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="afb4f-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="afb4f-146">Dopuszczalne wartości tego parametru są następujące: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="afb4f-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="afb4f-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="afb4f-147">-UseConsumptionModel</span></span>
<span data-ttu-id="afb4f-148">Wskazuje, że rozliczenia aplikacji logiki korzysta z modelu opartego na zużyciu.</span><span class="sxs-lookup"><span data-stu-id="afb4f-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="afb4f-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afb4f-149">-Confirm</span></span>
<span data-ttu-id="afb4f-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb4f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb4f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb4f-151">-WhatIf</span></span>
<span data-ttu-id="afb4f-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb4f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb4f-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afb4f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb4f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb4f-154">CommonParameters</span></span>
<span data-ttu-id="afb4f-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb4f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb4f-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb4f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb4f-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afb4f-157">INPUTS</span></span>

### <span data-ttu-id="afb4f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="afb4f-158">System.String</span></span>

## <span data-ttu-id="afb4f-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afb4f-159">OUTPUTS</span></span>

### <span data-ttu-id="afb4f-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="afb4f-160">System.Object</span></span>

## <span data-ttu-id="afb4f-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afb4f-161">NOTES</span></span>

## <span data-ttu-id="afb4f-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afb4f-162">RELATED LINKS</span></span>

[<span data-ttu-id="afb4f-163">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="afb4f-163">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="afb4f-164">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="afb4f-164">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="afb4f-165">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="afb4f-165">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="afb4f-166">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="afb4f-166">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



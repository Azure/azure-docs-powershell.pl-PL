---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241338"
---
# <span data-ttu-id="41acc-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="41acc-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="41acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41acc-102">SYNOPSIS</span></span>
<span data-ttu-id="41acc-103">Aktualizuje właściwości istniejącego zasobu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="41acc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41acc-104">SYNTAX</span></span>

### <span data-ttu-id="41acc-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="41acc-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41acc-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="41acc-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41acc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="41acc-107">DESCRIPTION</span></span>
<span data-ttu-id="41acc-108">Polecenie Update-AzMlWebService cmdlet umożliwia aktualizowanie niestatycznych właściwości usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="41acc-109">Polecenie cmdlet działa jak operacja poprawek.</span><span class="sxs-lookup"><span data-stu-id="41acc-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="41acc-110">Przekaż tylko te właściwości, które chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="41acc-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="41acc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41acc-111">EXAMPLES</span></span>

### <span data-ttu-id="41acc-112">Przykład 1. Argumenty aktualizacji selektywnej</span><span class="sxs-lookup"><span data-stu-id="41acc-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="41acc-113">Tutaj zmieniamy opis, klucz dostępu podstawowego i włączamy zbiór diagnostyki dla wszystkich śledzenia w czasie wykonywania usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="41acc-114">Przykład 2. Aktualizacja oparta na wystąpieniu usługi sieci Web</span><span class="sxs-lookup"><span data-stu-id="41acc-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="41acc-115">W przykładzie najpierw jest ana definicja usługi sieci Web, która zawiera tylko pola do zaktualizowania, a następnie jest Update-AzMlWebService w celu ich zastosowania przy użyciu parametru ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="41acc-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="41acc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41acc-116">PARAMETERS</span></span>

### <span data-ttu-id="41acc-117">— Majątek</span><span class="sxs-lookup"><span data-stu-id="41acc-117">-Assets</span></span>
<span data-ttu-id="41acc-118">Zestaw środków trwałych (np. modułów, zestawów danych), które są usługą sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41acc-119">-DefaultProfile</span></span>
<span data-ttu-id="41acc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="41acc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41acc-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="41acc-121">-Description</span></span>
<span data-ttu-id="41acc-122">Nowa wartość w opisie usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-122">The new value for the web service's description.</span></span>
<span data-ttu-id="41acc-123">Jest to widoczne w schemacie interfejsu API Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="41acc-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-124">— Diagnostyka</span><span class="sxs-lookup"><span data-stu-id="41acc-124">-Diagnostics</span></span>
<span data-ttu-id="41acc-125">Ustawienia kontrolują zbiór danych śledzenia diagnostycznego dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="41acc-126">-Force</span></span>
<span data-ttu-id="41acc-127">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41acc-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="41acc-128">- Input</span><span class="sxs-lookup"><span data-stu-id="41acc-128">-Input</span></span>
<span data-ttu-id="41acc-129">Definicja danych wejściowych usługi sieci Web, dostarczana jako konstruowanie schematu Swagger.</span><span class="sxs-lookup"><span data-stu-id="41acc-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-130">— IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="41acc-130">-IsReadOnly</span></span>
<span data-ttu-id="41acc-131">Określa, że ta usługa sieci Web jest tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="41acc-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="41acc-132">Po jej skonfigurowaniu usługa sieci Web może być już aktualizowana, łącznie ze zmianą wartości tej właściwości, i można ją usunąć tylko.</span><span class="sxs-lookup"><span data-stu-id="41acc-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-133">— Klawisze</span><span class="sxs-lookup"><span data-stu-id="41acc-133">-Keys</span></span>
<span data-ttu-id="41acc-134">Aktualizuje co najmniej jeden z kluczy dostępu używanych do uwierzytelniania połączeń z interfejsami API środowiska uruchomieniowego usługi.</span><span class="sxs-lookup"><span data-stu-id="41acc-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41acc-135">-Name</span></span>
<span data-ttu-id="41acc-136">Nazwa zasobu usługi sieci Web do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="41acc-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-137">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="41acc-137">-Output</span></span>
<span data-ttu-id="41acc-138">Definicja danych wyjściowych usługi sieci Web, dostarczana jako konstruowanie schematu Swaggera.</span><span class="sxs-lookup"><span data-stu-id="41acc-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-139">— Pakiet</span><span class="sxs-lookup"><span data-stu-id="41acc-139">-Package</span></span>
<span data-ttu-id="41acc-140">Definicja pakietu wykresu definiującego tę usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="41acc-141">-Parameters</span></span>
<span data-ttu-id="41acc-142">Zestaw wartości parametrów globalnych zdefiniowanych dla usługi sieci Web, podany jako nazwa parametru globalnego — \> domyślny zbiór wartości.</span><span class="sxs-lookup"><span data-stu-id="41acc-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="41acc-143">Jeśli nie zostanie określona żadna wartość domyślna, parametr jest uznawany za wymagany.</span><span class="sxs-lookup"><span data-stu-id="41acc-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-144">—RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="41acc-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="41acc-145">Aktualizacje dotyczące konfiguracji punktu końcowego usługi w czasie rzeczywistym.</span><span class="sxs-lookup"><span data-stu-id="41acc-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41acc-146">-ResourceGroupName</span></span>
<span data-ttu-id="41acc-147">Grupa zasobów zawierająca usługę sieci Web do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="41acc-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="41acc-148">-ServiceUpdates</span></span>
<span data-ttu-id="41acc-149">Zestaw aktualizacji, które mają być stosowane do usługi sieci Web udostępnianej jako wystąpienie definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="41acc-150">Modyfikowane są tylko pola niestatyczne.</span><span class="sxs-lookup"><span data-stu-id="41acc-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="41acc-151">-StorageAccountKey</span></span>
<span data-ttu-id="41acc-152">Obraca klucz dostępu dla konta magazynu skojarzonego z usługą sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-153">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="41acc-153">-Title</span></span>
<span data-ttu-id="41acc-154">Nowa wartość tytułu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41acc-154">The new value for the web service's title.</span></span>
<span data-ttu-id="41acc-155">Jest to widoczne w schemacie interfejsu API Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="41acc-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41acc-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41acc-156">-Confirm</span></span>
<span data-ttu-id="41acc-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41acc-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41acc-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41acc-158">-WhatIf</span></span>
<span data-ttu-id="41acc-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41acc-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41acc-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41acc-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41acc-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41acc-161">CommonParameters</span></span>
<span data-ttu-id="41acc-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41acc-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41acc-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41acc-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41acc-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41acc-164">INPUTS</span></span>

### <span data-ttu-id="41acc-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="41acc-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="41acc-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41acc-166">OUTPUTS</span></span>

### <span data-ttu-id="41acc-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="41acc-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="41acc-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41acc-168">NOTES</span></span>
<span data-ttu-id="41acc-169">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="41acc-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="41acc-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41acc-170">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362504"
---
# <span data-ttu-id="99062-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="99062-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="99062-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99062-102">SYNOPSIS</span></span>
<span data-ttu-id="99062-103">Aktualizuje właściwości istniejącego zasobu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="99062-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99062-104">SYNTAX</span></span>

### <span data-ttu-id="99062-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="99062-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99062-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="99062-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99062-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99062-107">DESCRIPTION</span></span>
<span data-ttu-id="99062-108">Polecenie cmdlet Update-AzMlWebService umożliwia zaktualizowanie właściwości niestatycznych usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="99062-109">Polecenie cmdlet działa jako operacja patch.</span><span class="sxs-lookup"><span data-stu-id="99062-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="99062-110">Przekazanie tylko właściwości, które mają zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="99062-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="99062-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99062-111">EXAMPLES</span></span>

### <span data-ttu-id="99062-112">Przykład 1: argumenty aktualizacji selektywnej</span><span class="sxs-lookup"><span data-stu-id="99062-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="99062-113">W tym miejscu zmienimy opis, podstawowy klucz dostępu i włączono zbieranie danych diagnostycznych dla wszystkich śladów w czasie wykonywania usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="99062-114">Przykład 2: Aktualizacja oparta na wystąpieniu usługi sieci Web</span><span class="sxs-lookup"><span data-stu-id="99062-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="99062-115">W przykładzie najpierw tworzona jest definicja usługi sieci Web, która zawiera tylko te pola, które mają zostać zaktualizowane, a następnie dzwoni Update-AzMlWebService, aby zastosować je przy użyciu parametru serviceupdates.</span><span class="sxs-lookup"><span data-stu-id="99062-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="99062-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99062-116">PARAMETERS</span></span>

### <span data-ttu-id="99062-117">-Majątek</span><span class="sxs-lookup"><span data-stu-id="99062-117">-Assets</span></span>
<span data-ttu-id="99062-118">Zestaw zasobów (na przykład moduły, zestawy danych), które tworzą usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="99062-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99062-119">-DefaultProfile</span></span>
<span data-ttu-id="99062-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="99062-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99062-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="99062-121">-Description</span></span>
<span data-ttu-id="99062-122">Nowa wartość opisu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-122">The new value for the web service's description.</span></span>
<span data-ttu-id="99062-123">Jest ona widoczna w schemacie API struktury Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="99062-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="99062-124">-Diagnostyka</span><span class="sxs-lookup"><span data-stu-id="99062-124">-Diagnostics</span></span>
<span data-ttu-id="99062-125">Ustawienia sterujące kolekcją śledzenia diagnostycznego dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="99062-126">-Force</span><span class="sxs-lookup"><span data-stu-id="99062-126">-Force</span></span>
<span data-ttu-id="99062-127">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99062-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="99062-128">— Dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="99062-128">-Input</span></span>
<span data-ttu-id="99062-129">Definicja wprowadzania danych przez usługę sieci Web, podana jako konstrukcja schematu struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="99062-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="99062-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="99062-130">-IsReadOnly</span></span>
<span data-ttu-id="99062-131">Określa, że ta usługa sieci Web jest tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="99062-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="99062-132">Po ustawieniu usługa sieci Web może być już aktualizowana, w tym zmienianie wartości tej właściwości, i można ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="99062-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="99062-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="99062-133">-Keys</span></span>
<span data-ttu-id="99062-134">Umożliwia zaktualizowanie jednego lub obu klawiszy dostępu używanych do uwierzytelniania połączeń z interfejsami API środowiska wykonawczego usługi.</span><span class="sxs-lookup"><span data-stu-id="99062-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="99062-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99062-135">-Name</span></span>
<span data-ttu-id="99062-136">Nazwa zasobu usługi sieci Web, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="99062-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="99062-137">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="99062-137">-Output</span></span>
<span data-ttu-id="99062-138">Definicja wyników (-y) usługi sieci Web, dostarczona jako konstrukcja schematu struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="99062-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="99062-139">-Package</span><span class="sxs-lookup"><span data-stu-id="99062-139">-Package</span></span>
<span data-ttu-id="99062-140">Definicja pakietu wykresu definiującego tę usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="99062-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="99062-141">-Parameters</span></span>
<span data-ttu-id="99062-142">Zestaw wartości parametrów globalnych zdefiniowanych dla usługi sieci Web, które są podawane jako globalna nazwa parametru — \> Kolekcja wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="99062-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="99062-143">Jeśli nie określono wartości domyślnej, parametr jest uznawany za wymagany.</span><span class="sxs-lookup"><span data-stu-id="99062-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="99062-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="99062-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="99062-145">Aktualizacje konfiguracji punktu końcowego czasu rzeczywistego usługi.</span><span class="sxs-lookup"><span data-stu-id="99062-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="99062-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99062-146">-ResourceGroupName</span></span>
<span data-ttu-id="99062-147">Grupa zasobów zawierająca usługę sieci Web, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="99062-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="99062-148">-Serviceupdates</span><span class="sxs-lookup"><span data-stu-id="99062-148">-ServiceUpdates</span></span>
<span data-ttu-id="99062-149">Zestaw aktualizacji, które mają zostać zastosowane do usługi sieci Web w postaci wystąpienia definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="99062-150">Modyfikowane są tylko pola niestatyczne.</span><span class="sxs-lookup"><span data-stu-id="99062-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="99062-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="99062-151">-StorageAccountKey</span></span>
<span data-ttu-id="99062-152">Obracanie klawisza dostępu do konta magazynu skojarzonego z usługą sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="99062-153">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="99062-153">-Title</span></span>
<span data-ttu-id="99062-154">Nowa wartość tytułu dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="99062-154">The new value for the web service's title.</span></span>
<span data-ttu-id="99062-155">Jest ona widoczna w schemacie API struktury Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="99062-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="99062-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99062-156">-Confirm</span></span>
<span data-ttu-id="99062-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99062-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99062-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99062-158">-WhatIf</span></span>
<span data-ttu-id="99062-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99062-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99062-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99062-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99062-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99062-161">CommonParameters</span></span>
<span data-ttu-id="99062-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99062-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99062-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99062-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99062-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99062-164">INPUTS</span></span>

### <span data-ttu-id="99062-165">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="99062-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="99062-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99062-166">OUTPUTS</span></span>

### <span data-ttu-id="99062-167">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="99062-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="99062-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99062-168">NOTES</span></span>
<span data-ttu-id="99062-169">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="99062-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="99062-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99062-170">RELATED LINKS</span></span>

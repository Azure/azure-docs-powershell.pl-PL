---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549148"
---
# <span data-ttu-id="aad80-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="aad80-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="aad80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aad80-102">SYNOPSIS</span></span>
<span data-ttu-id="aad80-103">Aktualizuje właściwości istniejącego zasobu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aad80-104">SYNTAX</span></span>

### <span data-ttu-id="aad80-105">Zaktualizuj określone właściwości.</span><span class="sxs-lookup"><span data-stu-id="aad80-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad80-106">Utwórz nową usługę sieci Web Azure ML z definicji wystąpienia usługi WebService.</span><span class="sxs-lookup"><span data-stu-id="aad80-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad80-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aad80-107">DESCRIPTION</span></span>
<span data-ttu-id="aad80-108">Polecenie cmdlet Update-AzureRmMlWebService umożliwia zaktualizowanie właściwości niestatycznych usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="aad80-109">Polecenie cmdlet działa jako operacja patch.</span><span class="sxs-lookup"><span data-stu-id="aad80-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="aad80-110">Przekazanie tylko właściwości, które mają zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="aad80-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="aad80-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aad80-111">EXAMPLES</span></span>

### <span data-ttu-id="aad80-112">--------------------------Przykład 1: argumenty aktualizacji selektywnej--------------------------</span><span class="sxs-lookup"><span data-stu-id="aad80-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="aad80-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="aad80-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="aad80-114">W tym miejscu zmienimy opis, podstawowy klucz dostępu i włączono zbieranie danych diagnostycznych dla wszystkich śladów w czasie wykonywania usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="aad80-115">--------------------------Przykład 2: Aktualizacja oparta na wystąpieniu usługi sieci Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="aad80-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="aad80-116">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="aad80-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="aad80-117">W przykładzie najpierw tworzona jest definicja usługi sieci Web, która zawiera tylko te pola, które mają zostać zaktualizowane, a następnie dzwoni Update-AzureRmMlWebService, aby zastosować je przy użyciu parametru serviceupdates.</span><span class="sxs-lookup"><span data-stu-id="aad80-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="aad80-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aad80-118">PARAMETERS</span></span>

### <span data-ttu-id="aad80-119">-Majątek</span><span class="sxs-lookup"><span data-stu-id="aad80-119">-Assets</span></span>
<span data-ttu-id="aad80-120">Zestaw zasobów (na przykład moduły, zestawy danych), które tworzą usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="aad80-121">-Description</span></span>
<span data-ttu-id="aad80-122">Nowa wartość opisu usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-122">The new value for the web service's description.</span></span>
<span data-ttu-id="aad80-123">Jest ona widoczna w schemacie API struktury Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="aad80-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-124">-Diagnostyka</span><span class="sxs-lookup"><span data-stu-id="aad80-124">-Diagnostics</span></span>
<span data-ttu-id="aad80-125">Ustawienia sterujące kolekcją śledzenia diagnostycznego dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-126">-Force</span><span class="sxs-lookup"><span data-stu-id="aad80-126">-Force</span></span>
<span data-ttu-id="aad80-127">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aad80-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aad80-128">— Dane wejściowe</span><span class="sxs-lookup"><span data-stu-id="aad80-128">-Input</span></span>
<span data-ttu-id="aad80-129">Definicja wprowadzania danych przez usługę sieci Web, podana jako konstrukcja schematu struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="aad80-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="aad80-130">-IsReadOnly</span></span>
<span data-ttu-id="aad80-131">Określa, że ta usługa sieci Web jest tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="aad80-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="aad80-132">Po ustawieniu usługa sieci Web może być już aktualizowana, w tym zmienianie wartości tej właściwości, i można ją usunąć.</span><span class="sxs-lookup"><span data-stu-id="aad80-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="aad80-133">-Keys</span></span>
<span data-ttu-id="aad80-134">Umożliwia zaktualizowanie jednego lub obu klawiszy dostępu używanych do uwierzytelniania połączeń z interfejsami API środowiska wykonawczego usługi.</span><span class="sxs-lookup"><span data-stu-id="aad80-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aad80-135">-Name</span></span>
<span data-ttu-id="aad80-136">Nazwa zasobu usługi sieci Web, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="aad80-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="aad80-137">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="aad80-137">-Output</span></span>
<span data-ttu-id="aad80-138">Definicja wyników (-y) usługi sieci Web, dostarczona jako konstrukcja schematu struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="aad80-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-139">-Package</span><span class="sxs-lookup"><span data-stu-id="aad80-139">-Package</span></span>
<span data-ttu-id="aad80-140">Definicja pakietu wykresu definiującego tę usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="aad80-141">-Parameters</span></span>
<span data-ttu-id="aad80-142">Zestaw wartości parametrów globalnych zdefiniowanych dla usługi sieci Web, które są podawane jako globalna nazwa parametru — \> Kolekcja wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="aad80-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="aad80-143">Jeśli nie określono wartości domyślnej, parametr jest uznawany za wymagany.</span><span class="sxs-lookup"><span data-stu-id="aad80-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad80-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="aad80-145">Aktualizacje konfiguracji punktu końcowego czasu rzeczywistego usługi.</span><span class="sxs-lookup"><span data-stu-id="aad80-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad80-146">-ResourceGroupName</span></span>
<span data-ttu-id="aad80-147">Grupa zasobów zawierająca usługę sieci Web, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="aad80-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="aad80-148">-Serviceupdates</span><span class="sxs-lookup"><span data-stu-id="aad80-148">-ServiceUpdates</span></span>
<span data-ttu-id="aad80-149">Zestaw aktualizacji, które mają zostać zastosowane do usługi sieci Web w postaci wystąpienia definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="aad80-150">Modyfikowane są tylko pola niestatyczne.</span><span class="sxs-lookup"><span data-stu-id="aad80-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aad80-151">-StorageAccountKey</span></span>
<span data-ttu-id="aad80-152">Obracanie klawisza dostępu do konta magazynu skojarzonego z usługą sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-153">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="aad80-153">-Title</span></span>
<span data-ttu-id="aad80-154">Nowa wartość tytułu dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-154">The new value for the web service's title.</span></span>
<span data-ttu-id="aad80-155">Jest ona widoczna w schemacie API struktury Swagger usługi.</span><span class="sxs-lookup"><span data-stu-id="aad80-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad80-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aad80-156">-Confirm</span></span>
<span data-ttu-id="aad80-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad80-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad80-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad80-158">-WhatIf</span></span>
<span data-ttu-id="aad80-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad80-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad80-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aad80-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad80-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad80-161">-DefaultProfile</span></span>
<span data-ttu-id="aad80-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aad80-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad80-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad80-163">CommonParameters</span></span>
<span data-ttu-id="aad80-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad80-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad80-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad80-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad80-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aad80-166">INPUTS</span></span>

### <span data-ttu-id="aad80-167">Usług</span><span class="sxs-lookup"><span data-stu-id="aad80-167">WebService</span></span>
<span data-ttu-id="aad80-168">Parametr "serviceupdates" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="aad80-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="aad80-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aad80-169">OUTPUTS</span></span>

### <span data-ttu-id="aad80-170">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="aad80-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="aad80-171">Skrócony opis usługi sieci Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="aad80-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="aad80-172">Podobny do opisu zwróconego przez wywołanie polecenia cmdlet Get-AzureRmMlWebService w istniejącej usłudze sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aad80-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="aad80-173">Ten opis nie zawiera poufnych właściwości, takich jak poświadczenia konta magazynu i klucze dostępu usługi.</span><span class="sxs-lookup"><span data-stu-id="aad80-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="aad80-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aad80-174">NOTES</span></span>
<span data-ttu-id="aad80-175">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="aad80-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="aad80-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aad80-176">RELATED LINKS</span></span>


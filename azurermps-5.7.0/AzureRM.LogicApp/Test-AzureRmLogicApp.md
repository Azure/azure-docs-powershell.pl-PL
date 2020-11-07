---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: c93cf0fdceebb3507a19c06ea5b6dda96fbc0656
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718917"
---
# <span data-ttu-id="2f4b9-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="2f4b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4b9-103">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f4b9-104">SYNTAX</span></span>

### <span data-ttu-id="2f4b9-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4b9-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f4b9-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f4b9-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f4b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2f4b9-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4b9-108">Polecenie cmdlet **test-AzureRmLogicApp** sprawdza poprawność definicji aplikacji logiki w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="2f4b9-109">Określ nazwę aplikacji logicznej, nazwę grupy zasobów, lokalizację, stan, identyfikator konta integracji lub parametry.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="2f4b9-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2f4b9-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2f4b9-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2f4b9-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2f4b9-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f4b9-114">EXAMPLES</span></span>

### <span data-ttu-id="2f4b9-115">Przykład 1: sprawdzanie poprawności aplikacji logiki przy użyciu ścieżek plików</span><span class="sxs-lookup"><span data-stu-id="2f4b9-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="2f4b9-116">To polecenie sprawdza poprawność aplikacji logicznej o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="2f4b9-117">Polecenie określa ścieżki plików definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="2f4b9-118">Przykład 2: sprawdzanie poprawności aplikacji logiki za pomocą obiektów</span><span class="sxs-lookup"><span data-stu-id="2f4b9-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="2f4b9-119">To polecenie sprawdza poprawność aplikacji logicznej o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="2f4b9-120">W tym poleceniu są określone obiekty definicje i parametry.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="2f4b9-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f4b9-121">PARAMETERS</span></span>

### <span data-ttu-id="2f4b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4b9-122">-DefaultProfile</span></span>
<span data-ttu-id="2f4b9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f4b9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-124">-Definicja</span><span class="sxs-lookup"><span data-stu-id="2f4b9-124">-Definition</span></span>
<span data-ttu-id="2f4b9-125">Określa definicję aplikacji logicznej jako obiektu lub ciągu w formacie notacji kodu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="2f4b9-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="2f4b9-126">-DefinitionFilePath</span></span>
<span data-ttu-id="2f4b9-127">Określa definicję aplikacji logicznej jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="2f4b9-128">-IntegrationAccountId</span></span>
<span data-ttu-id="2f4b9-129">Określa identyfikator konta integracyjnego dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-129">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f4b9-130">-Location</span></span>
<span data-ttu-id="2f4b9-131">Określa lokalizację aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="2f4b9-132">Wprowadź lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia USA lub południowo-zachodni.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="2f4b9-133">Aplikację logiczną można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-133">You can place a logic app in any location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f4b9-134">-Name</span></span>
<span data-ttu-id="2f4b9-135">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-135">Specifies the name of the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="2f4b9-136">-ParameterFilePath</span></span>
<span data-ttu-id="2f4b9-137">Określa ścieżkę pliku parametrów w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-137">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-138">— Parametry</span><span class="sxs-lookup"><span data-stu-id="2f4b9-138">-Parameters</span></span>
<span data-ttu-id="2f4b9-139">Określa obiekt kolekcji Parameters aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="2f4b9-140">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="2f4b9-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4b9-141">-ResourceGroupName</span></span>
<span data-ttu-id="2f4b9-142">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-142">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-143">-State</span><span class="sxs-lookup"><span data-stu-id="2f4b9-143">-State</span></span>
<span data-ttu-id="2f4b9-144">Określa stan aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="2f4b9-145">Dopuszczalne wartości tego parametru są następujące: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4b9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4b9-146">CommonParameters</span></span>
<span data-ttu-id="2f4b9-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4b9-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4b9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4b9-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f4b9-149">INPUTS</span></span>

### <span data-ttu-id="2f4b9-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2f4b9-150">None</span></span>
<span data-ttu-id="2f4b9-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2f4b9-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f4b9-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f4b9-152">OUTPUTS</span></span>

### <span data-ttu-id="2f4b9-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f4b9-153">System.Object</span></span>

## <span data-ttu-id="2f4b9-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f4b9-154">NOTES</span></span>

## <span data-ttu-id="2f4b9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f4b9-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f4b9-156">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-156">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="2f4b9-157">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-157">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="2f4b9-158">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-158">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="2f4b9-159">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-159">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="2f4b9-160">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2f4b9-160">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



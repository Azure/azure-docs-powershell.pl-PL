---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554345"
---
# <span data-ttu-id="45bd7-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="45bd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="45bd7-103">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="45bd7-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45bd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45bd7-104">SYNTAX</span></span>

### <span data-ttu-id="45bd7-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="45bd7-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45bd7-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="45bd7-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45bd7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="45bd7-107">DESCRIPTION</span></span>
<span data-ttu-id="45bd7-108">Polecenie cmdlet **test-AzureRmLogicApp** sprawdza poprawność definicji aplikacji logiki w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45bd7-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="45bd7-109">Określ nazwę aplikacji logicznej, nazwę grupy zasobów, lokalizację, stan, identyfikator konta integracji lub parametry.</span><span class="sxs-lookup"><span data-stu-id="45bd7-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="45bd7-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="45bd7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="45bd7-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="45bd7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="45bd7-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="45bd7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45bd7-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="45bd7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45bd7-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45bd7-114">EXAMPLES</span></span>

### <span data-ttu-id="45bd7-115">Przykład 1: sprawdzanie poprawności aplikacji logiki przy użyciu ścieżek plików</span><span class="sxs-lookup"><span data-stu-id="45bd7-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="45bd7-116">To polecenie sprawdza poprawność aplikacji logicznej o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45bd7-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="45bd7-117">Polecenie określa ścieżki plików definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="45bd7-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="45bd7-118">Przykład 2: sprawdzanie poprawności aplikacji logiki za pomocą obiektów</span><span class="sxs-lookup"><span data-stu-id="45bd7-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="45bd7-119">To polecenie sprawdza poprawność aplikacji logicznej o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45bd7-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="45bd7-120">W tym poleceniu są określone obiekty definicje i parametry.</span><span class="sxs-lookup"><span data-stu-id="45bd7-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="45bd7-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45bd7-121">PARAMETERS</span></span>

### <span data-ttu-id="45bd7-122">-Definicja</span><span class="sxs-lookup"><span data-stu-id="45bd7-122">-Definition</span></span>
<span data-ttu-id="45bd7-123">Określa definicję aplikacji logicznej jako obiektu lub ciągu w formacie notacji kodu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="45bd7-123">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bd7-124">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="45bd7-124">-DefinitionFilePath</span></span>
<span data-ttu-id="45bd7-125">Określa definicję aplikacji logicznej jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="45bd7-125">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bd7-126">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="45bd7-126">-IntegrationAccountId</span></span>
<span data-ttu-id="45bd7-127">Określa identyfikator konta integracyjnego dla aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="45bd7-127">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="45bd7-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="45bd7-128">-Location</span></span>
<span data-ttu-id="45bd7-129">Określa lokalizację aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="45bd7-129">Specifies the location of the logic app.</span></span>
<span data-ttu-id="45bd7-130">Wprowadź lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia USA lub południowo-zachodni.</span><span class="sxs-lookup"><span data-stu-id="45bd7-130">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="45bd7-131">Aplikację logiczną można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="45bd7-131">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="45bd7-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45bd7-132">-Name</span></span>
<span data-ttu-id="45bd7-133">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="45bd7-133">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bd7-134">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="45bd7-134">-ParameterFilePath</span></span>
<span data-ttu-id="45bd7-135">Określa ścieżkę pliku parametrów w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="45bd7-135">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="45bd7-136">— Parametry</span><span class="sxs-lookup"><span data-stu-id="45bd7-136">-Parameters</span></span>
<span data-ttu-id="45bd7-137">Określa obiekt kolekcji Parameters aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="45bd7-137">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="45bd7-138">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="45bd7-138">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="45bd7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bd7-139">-ResourceGroupName</span></span>
<span data-ttu-id="45bd7-140">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45bd7-140">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="45bd7-141">-State</span><span class="sxs-lookup"><span data-stu-id="45bd7-141">-State</span></span>
<span data-ttu-id="45bd7-142">Określa stan aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="45bd7-142">Specifies a state of the logic app.</span></span>
<span data-ttu-id="45bd7-143">Dopuszczalne wartości tego parametru są następujące: włączone i wyłączone.</span><span class="sxs-lookup"><span data-stu-id="45bd7-143">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="45bd7-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bd7-144">-DefaultProfile</span></span>
<span data-ttu-id="45bd7-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45bd7-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45bd7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bd7-146">CommonParameters</span></span>
<span data-ttu-id="45bd7-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bd7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bd7-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bd7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bd7-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45bd7-149">INPUTS</span></span>

## <span data-ttu-id="45bd7-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45bd7-150">OUTPUTS</span></span>

### <span data-ttu-id="45bd7-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="45bd7-151">System.Object</span></span>

## <span data-ttu-id="45bd7-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45bd7-152">NOTES</span></span>

## <span data-ttu-id="45bd7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45bd7-153">RELATED LINKS</span></span>

[<span data-ttu-id="45bd7-154">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-154">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="45bd7-155">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-155">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="45bd7-156">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-156">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="45bd7-157">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-157">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="45bd7-158">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="45bd7-158">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



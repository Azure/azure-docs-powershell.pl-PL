---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180346"
---
# <span data-ttu-id="c20b7-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="c20b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c20b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c20b7-103">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="c20b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c20b7-104">SYNTAX</span></span>

### <span data-ttu-id="c20b7-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c20b7-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c20b7-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c20b7-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c20b7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c20b7-107">DESCRIPTION</span></span>
<span data-ttu-id="c20b7-108">Polecenie **cmdlet Test-AzLogicApp** sprawdza poprawność definicji aplikacji logiki w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="c20b7-109">Określ nazwę aplikacji logiki, nazwę grupy zasobów, lokalizację, województwo, identyfikator konta integracji lub parametry.</span><span class="sxs-lookup"><span data-stu-id="c20b7-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="c20b7-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="c20b7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c20b7-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c20b7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c20b7-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="c20b7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c20b7-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="c20b7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c20b7-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c20b7-114">EXAMPLES</span></span>

### <span data-ttu-id="c20b7-115">Przykład 1. Sprawdzanie poprawności aplikacji logiki przy użyciu ścieżek plików</span><span class="sxs-lookup"><span data-stu-id="c20b7-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="c20b7-116">To polecenie sprawdza poprawność aplikacji logiki o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="c20b7-117">To polecenie określa ścieżki plików definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="c20b7-118">Przykład 2. Sprawdzanie poprawności aplikacji logiki przy użyciu obiektów</span><span class="sxs-lookup"><span data-stu-id="c20b7-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="c20b7-119">To polecenie sprawdza poprawność aplikacji logiki o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="c20b7-120">To polecenie określa obiekty definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="c20b7-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c20b7-121">Example 3</span></span>

<span data-ttu-id="c20b7-122">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-122">Validates a logic app definition.</span></span> <span data-ttu-id="c20b7-123">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="c20b7-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="c20b7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c20b7-124">PARAMETERS</span></span>

### <span data-ttu-id="c20b7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20b7-125">-DefaultProfile</span></span>
<span data-ttu-id="c20b7-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c20b7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c20b7-127">—Definicja</span><span class="sxs-lookup"><span data-stu-id="c20b7-127">-Definition</span></span>
<span data-ttu-id="c20b7-128">Określa definicję aplikacji logiki jako obiektu lub ciągu w formacie JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="c20b7-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c20b7-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="c20b7-129">-DefinitionFilePath</span></span>
<span data-ttu-id="c20b7-130">Określa definicję aplikacji logiki jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="c20b7-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="c20b7-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="c20b7-131">-IntegrationAccountId</span></span>
<span data-ttu-id="c20b7-132">Określa identyfikator konta integracji dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="c20b7-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c20b7-133">-Location</span></span>
<span data-ttu-id="c20b7-134">Określa lokalizację aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="c20b7-135">Wprowadź lokalizację centrum danych platformy Azure, taką jak Stany Zjednoczone i Azja Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="c20b7-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="c20b7-136">Aplikację logiki można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c20b7-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="c20b7-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c20b7-137">-Name</span></span>
<span data-ttu-id="c20b7-138">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="c20b7-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="c20b7-139">-ParameterFilePath</span></span>
<span data-ttu-id="c20b7-140">Określa ścieżkę pliku parametrów sformatowanych jako JSON.</span><span class="sxs-lookup"><span data-stu-id="c20b7-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="c20b7-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="c20b7-141">-Parameters</span></span>
<span data-ttu-id="c20b7-142">Określa obiekt kolekcji parametrów aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="c20b7-143">Określ tabelę \<string\> skrótów, słownik lub \<string, WorkflowParameter\> słownik.</span><span class="sxs-lookup"><span data-stu-id="c20b7-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="c20b7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c20b7-144">-ResourceGroupName</span></span>
<span data-ttu-id="c20b7-145">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c20b7-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c20b7-146">— województwo</span><span class="sxs-lookup"><span data-stu-id="c20b7-146">-State</span></span>
<span data-ttu-id="c20b7-147">Określa stan aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c20b7-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="c20b7-148">Dopuszczalne wartości dla tego parametru to: Włączone i Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="c20b7-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="c20b7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20b7-149">CommonParameters</span></span>
<span data-ttu-id="c20b7-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c20b7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20b7-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20b7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20b7-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c20b7-152">INPUTS</span></span>

### <span data-ttu-id="c20b7-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c20b7-153">System.String</span></span>

## <span data-ttu-id="c20b7-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c20b7-154">OUTPUTS</span></span>

### <span data-ttu-id="c20b7-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="c20b7-155">System.Void</span></span>

## <span data-ttu-id="c20b7-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c20b7-156">NOTES</span></span>

## <span data-ttu-id="c20b7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c20b7-157">RELATED LINKS</span></span>

[<span data-ttu-id="c20b7-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="c20b7-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c20b7-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c20b7-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="c20b7-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20b7-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



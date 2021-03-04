---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: 6639a397c97be35565d374279b2981fa2b1eabd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952369"
---
# <span data-ttu-id="0a22f-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="0a22f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a22f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a22f-103">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="0a22f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a22f-104">SYNTAX</span></span>

### <span data-ttu-id="0a22f-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a22f-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a22f-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a22f-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a22f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a22f-107">DESCRIPTION</span></span>
<span data-ttu-id="0a22f-108">Polecenie **cmdlet Test-AzLogicApp** sprawdza poprawność definicji aplikacji logiki w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="0a22f-109">Określ nazwę aplikacji logiki, nazwę grupy zasobów, lokalizację, województwo, identyfikator konta integracji lub parametry.</span><span class="sxs-lookup"><span data-stu-id="0a22f-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="0a22f-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="0a22f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0a22f-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="0a22f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0a22f-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="0a22f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a22f-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="0a22f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a22f-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a22f-114">EXAMPLES</span></span>

### <span data-ttu-id="0a22f-115">Przykład 1. Sprawdzanie poprawności aplikacji logiki przy użyciu ścieżek plików</span><span class="sxs-lookup"><span data-stu-id="0a22f-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="0a22f-116">To polecenie sprawdza poprawność aplikacji logiki o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0a22f-117">To polecenie określa ścieżki plików definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="0a22f-118">Przykład 2. Sprawdzanie poprawności aplikacji logiki przy użyciu obiektów</span><span class="sxs-lookup"><span data-stu-id="0a22f-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="0a22f-119">To polecenie sprawdza poprawność aplikacji logiki o nazwie LogicApp01 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="0a22f-120">To polecenie określa obiekty definicji i parametrów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="0a22f-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0a22f-121">Example 3</span></span>

<span data-ttu-id="0a22f-122">Sprawdza poprawność definicji aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-122">Validates a logic app definition.</span></span> <span data-ttu-id="0a22f-123">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="0a22f-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="0a22f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a22f-124">PARAMETERS</span></span>

### <span data-ttu-id="0a22f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a22f-125">-DefaultProfile</span></span>
<span data-ttu-id="0a22f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0a22f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a22f-127">—Definicja</span><span class="sxs-lookup"><span data-stu-id="0a22f-127">-Definition</span></span>
<span data-ttu-id="0a22f-128">Określa definicję aplikacji logiki jako obiektu lub ciągu w formacie JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="0a22f-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="0a22f-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="0a22f-129">-DefinitionFilePath</span></span>
<span data-ttu-id="0a22f-130">Określa definicję aplikacji logiki jako ścieżkę pliku definicji w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="0a22f-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="0a22f-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="0a22f-131">-IntegrationAccountId</span></span>
<span data-ttu-id="0a22f-132">Określa identyfikator konta integracji dla aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="0a22f-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0a22f-133">-Location</span></span>
<span data-ttu-id="0a22f-134">Określa lokalizację aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="0a22f-135">Wprowadź lokalizację centrum danych platformy Azure, taką jak Stany Zjednoczone i Azja Południowo-Wschodnia.</span><span class="sxs-lookup"><span data-stu-id="0a22f-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="0a22f-136">Aplikację logiki można umieścić w dowolnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0a22f-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="0a22f-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0a22f-137">-Name</span></span>
<span data-ttu-id="0a22f-138">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="0a22f-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="0a22f-139">-ParameterFilePath</span></span>
<span data-ttu-id="0a22f-140">Określa ścieżkę pliku sformatowanych parametrów JSON.</span><span class="sxs-lookup"><span data-stu-id="0a22f-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="0a22f-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="0a22f-141">-Parameters</span></span>
<span data-ttu-id="0a22f-142">Określa obiekt kolekcji parametrów aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0a22f-143">Określ tabelę skrótu, słownik \<string\> lub \<string, WorkflowParameter\> słownik.</span><span class="sxs-lookup"><span data-stu-id="0a22f-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="0a22f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a22f-144">-ResourceGroupName</span></span>
<span data-ttu-id="0a22f-145">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a22f-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0a22f-146">— województwo</span><span class="sxs-lookup"><span data-stu-id="0a22f-146">-State</span></span>
<span data-ttu-id="0a22f-147">Określa stan aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="0a22f-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="0a22f-148">Dopuszczalne wartości dla tego parametru to: Włączone i Wyłączone.</span><span class="sxs-lookup"><span data-stu-id="0a22f-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="0a22f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a22f-149">CommonParameters</span></span>
<span data-ttu-id="0a22f-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a22f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a22f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a22f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a22f-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a22f-152">INPUTS</span></span>

### <span data-ttu-id="0a22f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0a22f-153">System.String</span></span>

## <span data-ttu-id="0a22f-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a22f-154">OUTPUTS</span></span>

### <span data-ttu-id="0a22f-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="0a22f-155">System.Void</span></span>

## <span data-ttu-id="0a22f-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a22f-156">NOTES</span></span>

## <span data-ttu-id="0a22f-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a22f-157">RELATED LINKS</span></span>

[<span data-ttu-id="0a22f-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="0a22f-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="0a22f-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="0a22f-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="0a22f-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a22f-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 23dd1ba36a634e1b1d49e4623a9c652cda5bab27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867671"
---
# <span data-ttu-id="b2d78-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b2d78-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="b2d78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2d78-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d78-103">Tworzy schemat konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="b2d78-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="b2d78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2d78-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2d78-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d78-106">Polecenie cmdlet **New-AzIntegrationAccountSchema** umożliwia utworzenie schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="b2d78-107">To polecenie cmdlet zwraca obiekt reprezentujący schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="b2d78-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę schematu i definicję schematu.</span><span class="sxs-lookup"><span data-stu-id="b2d78-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="b2d78-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="b2d78-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b2d78-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="b2d78-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b2d78-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="b2d78-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b2d78-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b2d78-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b2d78-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="b2d78-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b2d78-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2d78-114">EXAMPLES</span></span>

### <span data-ttu-id="b2d78-115">Przykład 1. Tworzenie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="b2d78-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="b2d78-116">To polecenie tworzy schemat kont integracyjnych o nazwie IntegrationAccountSchema1 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2d78-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="b2d78-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2d78-117">PARAMETERS</span></span>

### <span data-ttu-id="b2d78-118">-Type</span><span class="sxs-lookup"><span data-stu-id="b2d78-118">-ContentType</span></span>
<span data-ttu-id="b2d78-119">Określa typ zawartości dla schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="b2d78-120">To polecenie cmdlet obsługuje aplikację Application/XML jako typ zawartości mapy.</span><span class="sxs-lookup"><span data-stu-id="b2d78-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b2d78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d78-121">-DefaultProfile</span></span>
<span data-ttu-id="b2d78-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b2d78-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2d78-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b2d78-123">-Metadata</span></span>
<span data-ttu-id="b2d78-124">Określa obiekt metadanych dla schematu.</span><span class="sxs-lookup"><span data-stu-id="b2d78-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="b2d78-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2d78-125">-Name</span></span>
<span data-ttu-id="b2d78-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d78-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d78-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2d78-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2d78-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b2d78-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="b2d78-129">-SchemaDefinition</span></span>
<span data-ttu-id="b2d78-130">Określa obiekt definicji dla schematu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="b2d78-131">Określ ten parametr lub parametr *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="b2d78-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="b2d78-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="b2d78-132">-SchemaFilePath</span></span>
<span data-ttu-id="b2d78-133">Określa ścieżkę pliku definicji dla schematu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="b2d78-134">Określ ten parametr lub parametr *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="b2d78-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="b2d78-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b2d78-135">-SchemaName</span></span>
<span data-ttu-id="b2d78-136">Określa nazwę schematu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="b2d78-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="b2d78-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="b2d78-137">-SchemaType</span></span>
<span data-ttu-id="b2d78-138">Umożliwia określenie typu schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b2d78-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="b2d78-139">Ten parametr obsługuje język XML jako typ.</span><span class="sxs-lookup"><span data-stu-id="b2d78-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d78-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2d78-140">-Confirm</span></span>
<span data-ttu-id="b2d78-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2d78-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d78-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d78-142">-WhatIf</span></span>
<span data-ttu-id="b2d78-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2d78-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d78-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2d78-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d78-145">CommonParameters</span></span>
<span data-ttu-id="b2d78-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d78-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d78-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d78-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2d78-148">INPUTS</span></span>

### <span data-ttu-id="b2d78-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b2d78-149">System.String</span></span>

## <span data-ttu-id="b2d78-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2d78-150">OUTPUTS</span></span>

### <span data-ttu-id="b2d78-151">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b2d78-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="b2d78-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2d78-152">NOTES</span></span>

## <span data-ttu-id="b2d78-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2d78-153">RELATED LINKS</span></span>

[<span data-ttu-id="b2d78-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b2d78-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="b2d78-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b2d78-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="b2d78-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b2d78-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)



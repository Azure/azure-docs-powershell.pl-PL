---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 908c75e2eeb71e864fcdf633511b8eb1c4147401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974817"
---
# <span data-ttu-id="fbe6b-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe6b-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="fbe6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe6b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe6b-103">Tworzy schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="fbe6b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbe6b-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe6b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbe6b-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe6b-106">Polecenie **cmdlet New-AzIntegrationAccountSchema** tworzy schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="fbe6b-107">To polecenie cmdlet zwraca obiekt reprezentujący schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="fbe6b-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę schematu i definicję schematu.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="fbe6b-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="fbe6b-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fbe6b-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fbe6b-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fbe6b-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fbe6b-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbe6b-114">EXAMPLES</span></span>

### <span data-ttu-id="fbe6b-115">Przykład 1. Tworzenie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="fbe6b-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="fbe6b-116">To polecenie tworzy schemat konta integracji o nazwie IntegrationAccountSchema1 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="fbe6b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe6b-117">PARAMETERS</span></span>

### <span data-ttu-id="fbe6b-118">- ContentType</span><span class="sxs-lookup"><span data-stu-id="fbe6b-118">-ContentType</span></span>
<span data-ttu-id="fbe6b-119">Określa typ zawartości schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="fbe6b-120">To polecenie cmdlet obsługuje dane typu zawartości aplikacji/xml jako mapy.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="fbe6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe6b-121">-DefaultProfile</span></span>
<span data-ttu-id="fbe6b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fbe6b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe6b-123">— Metadane</span><span class="sxs-lookup"><span data-stu-id="fbe6b-123">-Metadata</span></span>
<span data-ttu-id="fbe6b-124">Określa obiekt metadanych schematu.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="fbe6b-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fbe6b-125">-Name</span></span>
<span data-ttu-id="fbe6b-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="fbe6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbe6b-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fbe6b-129">- SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="fbe6b-129">-SchemaDefinition</span></span>
<span data-ttu-id="fbe6b-130">Określa obiekt definicji dla schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="fbe6b-131">Określ ten parametr lub *parametr SchemaFilePath.*</span><span class="sxs-lookup"><span data-stu-id="fbe6b-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="fbe6b-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="fbe6b-132">-SchemaFilePath</span></span>
<span data-ttu-id="fbe6b-133">Określa ścieżkę pliku definicji schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="fbe6b-134">Określ ten parametr lub *parametr SchemaDefinition.*</span><span class="sxs-lookup"><span data-stu-id="fbe6b-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="fbe6b-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fbe6b-135">-SchemaName</span></span>
<span data-ttu-id="fbe6b-136">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="fbe6b-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="fbe6b-137">-SchemaType</span></span>
<span data-ttu-id="fbe6b-138">Określa typ schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="fbe6b-139">Ten parametr obsługuje typ danych Xml.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="fbe6b-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbe6b-140">-Confirm</span></span>
<span data-ttu-id="fbe6b-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe6b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe6b-142">-WhatIf</span></span>
<span data-ttu-id="fbe6b-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe6b-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe6b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe6b-145">CommonParameters</span></span>
<span data-ttu-id="fbe6b-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe6b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe6b-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe6b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe6b-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe6b-148">INPUTS</span></span>

### <span data-ttu-id="fbe6b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe6b-149">System.String</span></span>

## <span data-ttu-id="fbe6b-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe6b-150">OUTPUTS</span></span>

### <span data-ttu-id="fbe6b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe6b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="fbe6b-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbe6b-152">NOTES</span></span>

## <span data-ttu-id="fbe6b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbe6b-153">RELATED LINKS</span></span>

[<span data-ttu-id="fbe6b-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe6b-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="fbe6b-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe6b-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="fbe6b-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe6b-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)



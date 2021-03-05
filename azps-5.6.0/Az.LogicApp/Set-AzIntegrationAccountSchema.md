---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: cc1c146209758b3ddac9e4b72dcee77e1accf8a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983105"
---
# <span data-ttu-id="9b7ef-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b7ef-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="9b7ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7ef-103">Modyfikuje schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="9b7ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b7ef-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b7ef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b7ef-105">DESCRIPTION</span></span>
<span data-ttu-id="9b7ef-106">Polecenie **cmdlet Set-AzIntegrationAccountSchema** modyfikuje schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="9b7ef-107">To polecenie cmdlet zwraca obiekt reprezentujący schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="9b7ef-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="9b7ef-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="9b7ef-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9b7ef-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9b7ef-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9b7ef-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9b7ef-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b7ef-114">EXAMPLES</span></span>

### <span data-ttu-id="9b7ef-115">Przykład 1. Modyfikowanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="9b7ef-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="9b7ef-116">To polecenie modyfikuje schemat konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="9b7ef-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b7ef-117">PARAMETERS</span></span>

### <span data-ttu-id="9b7ef-118">- ContentType</span><span class="sxs-lookup"><span data-stu-id="9b7ef-118">-ContentType</span></span>
<span data-ttu-id="9b7ef-119">Określa typ zawartości schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="9b7ef-120">To polecenie cmdlet obsługuje dane typu zawartości aplikacji/xml jako mapy.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="9b7ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7ef-121">-DefaultProfile</span></span>
<span data-ttu-id="9b7ef-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9b7ef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b7ef-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9b7ef-123">-Force</span></span>
<span data-ttu-id="9b7ef-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b7ef-125">— Metadane</span><span class="sxs-lookup"><span data-stu-id="9b7ef-125">-Metadata</span></span>
<span data-ttu-id="9b7ef-126">Określa obiekt metadanych schematu.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="9b7ef-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b7ef-127">-Name</span></span>
<span data-ttu-id="9b7ef-128">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9b7ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b7ef-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b7ef-131">- SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="9b7ef-131">-SchemaDefinition</span></span>
<span data-ttu-id="9b7ef-132">Określa obiekt definicji dla schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="9b7ef-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="9b7ef-133">-SchemaFilePath</span></span>
<span data-ttu-id="9b7ef-134">Określa ścieżkę pliku definicji schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="9b7ef-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9b7ef-135">-SchemaName</span></span>
<span data-ttu-id="9b7ef-136">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="9b7ef-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="9b7ef-137">-SchemaType</span></span>
<span data-ttu-id="9b7ef-138">Określa typ schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="9b7ef-139">Ten parametr obsługuje typ danych Xml.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="9b7ef-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b7ef-140">-Confirm</span></span>
<span data-ttu-id="9b7ef-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7ef-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7ef-142">-WhatIf</span></span>
<span data-ttu-id="9b7ef-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b7ef-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7ef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7ef-145">CommonParameters</span></span>
<span data-ttu-id="9b7ef-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7ef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7ef-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7ef-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7ef-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b7ef-148">INPUTS</span></span>

### <span data-ttu-id="9b7ef-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9b7ef-149">System.String</span></span>

## <span data-ttu-id="9b7ef-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b7ef-150">OUTPUTS</span></span>

### <span data-ttu-id="9b7ef-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b7ef-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="9b7ef-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b7ef-152">NOTES</span></span>

## <span data-ttu-id="9b7ef-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b7ef-153">RELATED LINKS</span></span>

[<span data-ttu-id="9b7ef-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b7ef-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9b7ef-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b7ef-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9b7ef-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b7ef-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)



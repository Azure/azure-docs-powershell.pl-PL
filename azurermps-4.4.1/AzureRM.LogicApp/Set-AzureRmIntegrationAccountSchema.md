---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: cedd95d235abc6e114359de63dfbf1f4e58f26c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553231"
---
# <span data-ttu-id="a7f75-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a7f75-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="a7f75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7f75-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f75-103">Modyfikuje schemat kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="a7f75-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7f75-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7f75-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7f75-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f75-106">Polecenie cmdlet **Set-AzureRmIntegrationAccountSchema** modyfikuje schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="a7f75-107">To polecenie cmdlet zwraca obiekt reprezentujący schemat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="a7f75-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="a7f75-108">Specify the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="a7f75-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="a7f75-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="a7f75-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a7f75-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a7f75-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="a7f75-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a7f75-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="a7f75-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a7f75-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="a7f75-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a7f75-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7f75-114">EXAMPLES</span></span>

### <span data-ttu-id="a7f75-115">Przykład 1. Modyfikowanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="a7f75-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="a7f75-116">To polecenie modyfikuje schemat konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="a7f75-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="a7f75-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7f75-117">PARAMETERS</span></span>

### <span data-ttu-id="a7f75-118">-Type</span><span class="sxs-lookup"><span data-stu-id="a7f75-118">-ContentType</span></span>
<span data-ttu-id="a7f75-119">Określa typ zawartości dla schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="a7f75-120">To polecenie cmdlet obsługuje aplikację Application/XML jako typ zawartości mapy.</span><span class="sxs-lookup"><span data-stu-id="a7f75-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="a7f75-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a7f75-121">-Force</span></span>
<span data-ttu-id="a7f75-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a7f75-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7f75-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a7f75-123">-Metadata</span></span>
<span data-ttu-id="a7f75-124">Określa obiekt metadanych dla schematu.</span><span class="sxs-lookup"><span data-stu-id="a7f75-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="a7f75-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a7f75-125">-Name</span></span>
<span data-ttu-id="a7f75-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-126">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="a7f75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f75-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7f75-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7f75-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a7f75-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="a7f75-129">-SchemaDefinition</span></span>
<span data-ttu-id="a7f75-130">Określa obiekt definicji dla schematu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-130">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="a7f75-131">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="a7f75-131">-SchemaFilePath</span></span>
<span data-ttu-id="a7f75-132">Określa ścieżkę pliku definicji dla schematu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-132">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="a7f75-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a7f75-133">-SchemaName</span></span>
<span data-ttu-id="a7f75-134">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-134">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="a7f75-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="a7f75-135">-SchemaType</span></span>
<span data-ttu-id="a7f75-136">Umożliwia określenie typu schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7f75-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="a7f75-137">Ten parametr obsługuje język XML jako typ.</span><span class="sxs-lookup"><span data-stu-id="a7f75-137">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="a7f75-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7f75-138">-Confirm</span></span>
<span data-ttu-id="a7f75-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f75-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f75-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f75-140">-WhatIf</span></span>
<span data-ttu-id="a7f75-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f75-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f75-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7f75-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f75-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f75-143">-DefaultProfile</span></span>
<span data-ttu-id="a7f75-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f75-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f75-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f75-145">CommonParameters</span></span>
<span data-ttu-id="a7f75-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f75-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f75-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f75-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f75-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7f75-148">INPUTS</span></span>

## <span data-ttu-id="a7f75-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7f75-149">OUTPUTS</span></span>

### <span data-ttu-id="a7f75-150">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a7f75-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="a7f75-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7f75-151">NOTES</span></span>

## <span data-ttu-id="a7f75-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7f75-152">RELATED LINKS</span></span>

[<span data-ttu-id="a7f75-153">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a7f75-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a7f75-154">Nowe — AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a7f75-154">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a7f75-155">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a7f75-155">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)


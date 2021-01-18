---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501454"
---
# <span data-ttu-id="1d11a-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1d11a-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="1d11a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d11a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d11a-103">Umożliwia utworzenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-103">Creates an integration account map.</span></span>

## <span data-ttu-id="1d11a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d11a-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d11a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d11a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d11a-106">Polecenie cmdlet **New-AzIntegrationAccountMap** umożliwia utworzenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="1d11a-107">To polecenie cmdlet zwraca obiekt reprezentujący mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="1d11a-108">Określanie nazwy konta integracji, nazwy grupy zasobów, nazwy mapy i definicji mapy.</span><span class="sxs-lookup"><span data-stu-id="1d11a-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="1d11a-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="1d11a-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1d11a-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="1d11a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1d11a-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1d11a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1d11a-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="1d11a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1d11a-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="1d11a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1d11a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d11a-114">EXAMPLES</span></span>

### <span data-ttu-id="1d11a-115">Przykład 1. Tworzenie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="1d11a-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="1d11a-116">To polecenie powoduje utworzenie mapy konta integracji w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d11a-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="1d11a-117">Polecenie Określa definicję mapy przechowywaną w zmiennej $MapContent za pomocą poprzedniego polecenia.</span><span class="sxs-lookup"><span data-stu-id="1d11a-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="1d11a-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1d11a-118">Example 2</span></span>

<span data-ttu-id="1d11a-119">Umożliwia utworzenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-119">Creates an integration account map.</span></span> <span data-ttu-id="1d11a-120">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="1d11a-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="1d11a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d11a-121">PARAMETERS</span></span>

### <span data-ttu-id="1d11a-122">-Type</span><span class="sxs-lookup"><span data-stu-id="1d11a-122">-ContentType</span></span>
<span data-ttu-id="1d11a-123">Określa typ zawartości mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="1d11a-124">To polecenie cmdlet obsługuje aplikację Application/XML jako typ zawartości mapy.</span><span class="sxs-lookup"><span data-stu-id="1d11a-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="1d11a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d11a-125">-DefaultProfile</span></span>
<span data-ttu-id="1d11a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1d11a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d11a-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="1d11a-127">-MapDefinition</span></span>
<span data-ttu-id="1d11a-128">Określa obiekt definicji dla mapy kont integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="1d11a-129">Określ ten parametr lub parametr *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="1d11a-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="1d11a-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="1d11a-130">-MapFilePath</span></span>
<span data-ttu-id="1d11a-131">Określa ścieżkę pliku definicji mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="1d11a-132">Określ ten parametr lub parametr *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="1d11a-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="1d11a-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="1d11a-133">-MapName</span></span>
<span data-ttu-id="1d11a-134">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="1d11a-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="1d11a-135">-MapType</span></span>
<span data-ttu-id="1d11a-136">Umożliwia określenie typu mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1d11a-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="1d11a-137">To polecenie cmdlet obsługuje język XSLT jako typ mapy.</span><span class="sxs-lookup"><span data-stu-id="1d11a-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d11a-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1d11a-138">-Metadata</span></span>
<span data-ttu-id="1d11a-139">Określa obiekt metadanych mapy.</span><span class="sxs-lookup"><span data-stu-id="1d11a-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="1d11a-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d11a-140">-Name</span></span>
<span data-ttu-id="1d11a-141">Określa nazwę konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="1d11a-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="1d11a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d11a-142">-ResourceGroupName</span></span>
<span data-ttu-id="1d11a-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d11a-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1d11a-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d11a-144">-Confirm</span></span>
<span data-ttu-id="1d11a-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d11a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d11a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d11a-146">-WhatIf</span></span>
<span data-ttu-id="1d11a-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d11a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d11a-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d11a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d11a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d11a-149">CommonParameters</span></span>
<span data-ttu-id="1d11a-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d11a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d11a-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d11a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d11a-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d11a-152">INPUTS</span></span>

### <span data-ttu-id="1d11a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1d11a-153">System.String</span></span>

## <span data-ttu-id="1d11a-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d11a-154">OUTPUTS</span></span>

### <span data-ttu-id="1d11a-155">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1d11a-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="1d11a-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d11a-156">NOTES</span></span>

## <span data-ttu-id="1d11a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d11a-157">RELATED LINKS</span></span>

[<span data-ttu-id="1d11a-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1d11a-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="1d11a-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1d11a-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="1d11a-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1d11a-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)



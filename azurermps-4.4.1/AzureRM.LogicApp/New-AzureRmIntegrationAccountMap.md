---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 2f6df9b28db7ad86a3c779a166df34c48d779621
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554357"
---
# <span data-ttu-id="ebfd3-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ebfd3-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="ebfd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfd3-103">Umożliwia utworzenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebfd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebfd3-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfd3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebfd3-105">DESCRIPTION</span></span>
<span data-ttu-id="ebfd3-106">Polecenie cmdlet **New-AzureRmIntegrationAccountMap** umożliwia utworzenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="ebfd3-107">To polecenie cmdlet zwraca obiekt reprezentujący mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="ebfd3-108">Określanie nazwy konta integracji, nazwy grupy zasobów, nazwy mapy i definicji mapy.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="ebfd3-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="ebfd3-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ebfd3-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ebfd3-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ebfd3-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ebfd3-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebfd3-114">EXAMPLES</span></span>

### <span data-ttu-id="ebfd3-115">Przykład 1. Tworzenie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="ebfd3-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="ebfd3-116">To polecenie powoduje utworzenie mapy konta integracji w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="ebfd3-117">Polecenie Określa definicję mapy przechowywaną w zmiennej $MapContent za pomocą poprzedniego polecenia.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="ebfd3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebfd3-118">PARAMETERS</span></span>

### <span data-ttu-id="ebfd3-119">-Type</span><span class="sxs-lookup"><span data-stu-id="ebfd3-119">-ContentType</span></span>
<span data-ttu-id="ebfd3-120">Określa typ zawartości mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="ebfd3-121">To polecenie cmdlet obsługuje aplikację Application/XML jako typ zawartości mapy.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="ebfd3-122">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="ebfd3-122">-MapDefinition</span></span>
<span data-ttu-id="ebfd3-123">Określa obiekt definicji dla mapy kont integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-123">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="ebfd3-124">Określ ten parametr lub parametr *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="ebfd3-124">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="ebfd3-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="ebfd3-125">-MapFilePath</span></span>
<span data-ttu-id="ebfd3-126">Określa ścieżkę pliku definicji mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-126">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="ebfd3-127">Określ ten parametr lub parametr *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="ebfd3-127">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="ebfd3-128">-MapName</span><span class="sxs-lookup"><span data-stu-id="ebfd3-128">-MapName</span></span>
<span data-ttu-id="ebfd3-129">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-129">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="ebfd3-130">-MapType</span><span class="sxs-lookup"><span data-stu-id="ebfd3-130">-MapType</span></span>
<span data-ttu-id="ebfd3-131">Umożliwia określenie typu mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-131">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="ebfd3-132">To polecenie cmdlet obsługuje język XSLT jako typ mapy.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-132">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfd3-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ebfd3-133">-Metadata</span></span>
<span data-ttu-id="ebfd3-134">Określa obiekt metadanych mapy.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-134">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="ebfd3-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebfd3-135">-Name</span></span>
<span data-ttu-id="ebfd3-136">Określa nazwę konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-136">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="ebfd3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfd3-137">-ResourceGroupName</span></span>
<span data-ttu-id="ebfd3-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebfd3-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebfd3-139">-Confirm</span></span>
<span data-ttu-id="ebfd3-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebfd3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfd3-141">-WhatIf</span></span>
<span data-ttu-id="ebfd3-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebfd3-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebfd3-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfd3-144">-DefaultProfile</span></span>
<span data-ttu-id="ebfd3-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebfd3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfd3-146">CommonParameters</span></span>
<span data-ttu-id="ebfd3-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfd3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfd3-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfd3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfd3-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebfd3-149">INPUTS</span></span>

## <span data-ttu-id="ebfd3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebfd3-150">OUTPUTS</span></span>

### <span data-ttu-id="ebfd3-151">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ebfd3-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="ebfd3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebfd3-152">NOTES</span></span>

## <span data-ttu-id="ebfd3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebfd3-153">RELATED LINKS</span></span>

[<span data-ttu-id="ebfd3-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ebfd3-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="ebfd3-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ebfd3-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="ebfd3-156">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ebfd3-156">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)



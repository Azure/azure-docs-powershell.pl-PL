---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: e2a66eef93d2ed59f78e492cac7fa7fac4dd0244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867607"
---
# <span data-ttu-id="45ada-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45ada-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="45ada-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45ada-102">SYNOPSIS</span></span>
<span data-ttu-id="45ada-103">Modyfikuje mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="45ada-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45ada-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45ada-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45ada-105">DESCRIPTION</span></span>
<span data-ttu-id="45ada-106">Polecenie cmdlet **Set-AzIntegrationAccountMap** modyfikuje mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="45ada-107">To polecenie cmdlet zwraca obiekt reprezentujący mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="45ada-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="45ada-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="45ada-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="45ada-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="45ada-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="45ada-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="45ada-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="45ada-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45ada-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="45ada-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45ada-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45ada-113">EXAMPLES</span></span>

### <span data-ttu-id="45ada-114">Przykład 1: modyfikowanie mapy kont integracji</span><span class="sxs-lookup"><span data-stu-id="45ada-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="45ada-115">To polecenie modyfikuje mapę konta integracji w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45ada-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="45ada-116">Polecenie Określa definicję mapy przechowywaną w zmiennej $MapContent za pomocą poprzedniego polecenia.</span><span class="sxs-lookup"><span data-stu-id="45ada-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="45ada-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45ada-117">PARAMETERS</span></span>

### <span data-ttu-id="45ada-118">-Type</span><span class="sxs-lookup"><span data-stu-id="45ada-118">-ContentType</span></span>
<span data-ttu-id="45ada-119">Określa typ zawartości mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="45ada-120">To polecenie cmdlet obsługuje aplikację Application/XML jako typ zawartości mapy.</span><span class="sxs-lookup"><span data-stu-id="45ada-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="45ada-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ada-121">-DefaultProfile</span></span>
<span data-ttu-id="45ada-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45ada-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45ada-123">-Force</span><span class="sxs-lookup"><span data-stu-id="45ada-123">-Force</span></span>
<span data-ttu-id="45ada-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45ada-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45ada-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="45ada-125">-MapDefinition</span></span>
<span data-ttu-id="45ada-126">Określa obiekt definicji dla mapy kont integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="45ada-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="45ada-127">-MapFilePath</span></span>
<span data-ttu-id="45ada-128">Określa ścieżkę pliku definicji mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="45ada-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="45ada-129">-MapName</span></span>
<span data-ttu-id="45ada-130">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="45ada-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="45ada-131">-MapType</span></span>
<span data-ttu-id="45ada-132">Umożliwia określenie typu mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="45ada-133">To polecenie cmdlet obsługuje język XSLT jako typ mapy.</span><span class="sxs-lookup"><span data-stu-id="45ada-133">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="45ada-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="45ada-134">-Metadata</span></span>
<span data-ttu-id="45ada-135">Określa obiekt metadanych mapy.</span><span class="sxs-lookup"><span data-stu-id="45ada-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="45ada-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45ada-136">-Name</span></span>
<span data-ttu-id="45ada-137">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="45ada-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="45ada-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ada-138">-ResourceGroupName</span></span>
<span data-ttu-id="45ada-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45ada-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="45ada-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45ada-140">-Confirm</span></span>
<span data-ttu-id="45ada-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ada-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ada-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ada-142">-WhatIf</span></span>
<span data-ttu-id="45ada-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ada-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ada-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45ada-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ada-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ada-145">CommonParameters</span></span>
<span data-ttu-id="45ada-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ada-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ada-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ada-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ada-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45ada-148">INPUTS</span></span>

### <span data-ttu-id="45ada-149">System. String</span><span class="sxs-lookup"><span data-stu-id="45ada-149">System.String</span></span>

## <span data-ttu-id="45ada-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45ada-150">OUTPUTS</span></span>

### <span data-ttu-id="45ada-151">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45ada-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="45ada-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45ada-152">NOTES</span></span>

## <span data-ttu-id="45ada-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45ada-153">RELATED LINKS</span></span>

[<span data-ttu-id="45ada-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45ada-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="45ada-155">Nowe — AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45ada-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="45ada-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45ada-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)



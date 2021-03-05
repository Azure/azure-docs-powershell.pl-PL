---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972737"
---
# <span data-ttu-id="99d3d-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="99d3d-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="99d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="99d3d-103">Modyfikuje mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="99d3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99d3d-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99d3d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="99d3d-106">Polecenie **cmdlet Set-AzIntegrationAccountMap** modyfikuje mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="99d3d-107">To polecenie cmdlet zwraca obiekt reprezentujący mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="99d3d-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="99d3d-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="99d3d-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="99d3d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="99d3d-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="99d3d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="99d3d-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="99d3d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="99d3d-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="99d3d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="99d3d-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99d3d-113">EXAMPLES</span></span>

### <span data-ttu-id="99d3d-114">Przykład 1. Modyfikowanie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="99d3d-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="99d3d-115">To polecenie modyfikuje mapę konta integracji w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="99d3d-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="99d3d-116">Polecenie określa definicję mapy przechowywaną w $MapContent danych za pomocą poprzedniego polecenia.</span><span class="sxs-lookup"><span data-stu-id="99d3d-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="99d3d-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99d3d-117">Example 2</span></span>

<span data-ttu-id="99d3d-118">Modyfikuje mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-118">Modifies an integration account map.</span></span> <span data-ttu-id="99d3d-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="99d3d-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="99d3d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99d3d-120">PARAMETERS</span></span>

### <span data-ttu-id="99d3d-121">- ContentType</span><span class="sxs-lookup"><span data-stu-id="99d3d-121">-ContentType</span></span>
<span data-ttu-id="99d3d-122">Określa typ zawartości mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="99d3d-123">To polecenie cmdlet obsługuje dane typu zawartości aplikacji/xml jako mapy.</span><span class="sxs-lookup"><span data-stu-id="99d3d-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="99d3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d3d-124">-DefaultProfile</span></span>
<span data-ttu-id="99d3d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="99d3d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99d3d-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="99d3d-126">-Force</span></span>
<span data-ttu-id="99d3d-127">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="99d3d-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99d3d-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="99d3d-128">-MapDefinition</span></span>
<span data-ttu-id="99d3d-129">Określa obiekt definicji dla mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="99d3d-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="99d3d-130">-MapFilePath</span></span>
<span data-ttu-id="99d3d-131">Określa ścieżkę pliku definicji mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="99d3d-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="99d3d-132">-MapName</span></span>
<span data-ttu-id="99d3d-133">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="99d3d-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="99d3d-134">-MapType</span></span>
<span data-ttu-id="99d3d-135">Określa typ mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="99d3d-136">To polecenie cmdlet obsługuje technologię Xslt jako typ mapy.</span><span class="sxs-lookup"><span data-stu-id="99d3d-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="99d3d-137">— Metadane</span><span class="sxs-lookup"><span data-stu-id="99d3d-137">-Metadata</span></span>
<span data-ttu-id="99d3d-138">Określa obiekt metadanych dla mapy.</span><span class="sxs-lookup"><span data-stu-id="99d3d-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="99d3d-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99d3d-139">-Name</span></span>
<span data-ttu-id="99d3d-140">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="99d3d-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="99d3d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d3d-141">-ResourceGroupName</span></span>
<span data-ttu-id="99d3d-142">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99d3d-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="99d3d-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99d3d-143">-Confirm</span></span>
<span data-ttu-id="99d3d-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99d3d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d3d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d3d-145">-WhatIf</span></span>
<span data-ttu-id="99d3d-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d3d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d3d-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99d3d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d3d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d3d-148">CommonParameters</span></span>
<span data-ttu-id="99d3d-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d3d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d3d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d3d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d3d-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99d3d-151">INPUTS</span></span>

### <span data-ttu-id="99d3d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="99d3d-152">System.String</span></span>

## <span data-ttu-id="99d3d-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99d3d-153">OUTPUTS</span></span>

### <span data-ttu-id="99d3d-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="99d3d-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="99d3d-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99d3d-155">NOTES</span></span>

## <span data-ttu-id="99d3d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99d3d-156">RELATED LINKS</span></span>

[<span data-ttu-id="99d3d-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="99d3d-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="99d3d-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="99d3d-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="99d3d-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="99d3d-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185210"
---
# <span data-ttu-id="cde38-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cde38-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="cde38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde38-102">SYNOPSIS</span></span>
<span data-ttu-id="cde38-103">Pobiera aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cde38-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="cde38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cde38-104">SYNTAX</span></span>

### <span data-ttu-id="cde38-105">ListWorkflows (Default)</span><span class="sxs-lookup"><span data-stu-id="cde38-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cde38-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="cde38-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde38-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cde38-107">DESCRIPTION</span></span>
<span data-ttu-id="cde38-108">Polecenie **cmdlet Get-AzLogicApp** pobiera aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="cde38-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="cde38-109">To polecenie cmdlet zwraca obiekt **przepływu** pracy.</span><span class="sxs-lookup"><span data-stu-id="cde38-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="cde38-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="cde38-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cde38-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="cde38-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cde38-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="cde38-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cde38-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="cde38-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cde38-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cde38-114">EXAMPLES</span></span>

### <span data-ttu-id="cde38-115">Przykład 1. Uzyskiwanie aplikacji logiki z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cde38-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="cde38-116">To polecenie pobiera aplikację logiczną z grupy zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="cde38-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="cde38-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde38-117">PARAMETERS</span></span>

### <span data-ttu-id="cde38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde38-118">-DefaultProfile</span></span>
<span data-ttu-id="cde38-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cde38-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cde38-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cde38-120">-Name</span></span>
<span data-ttu-id="cde38-121">Określa nazwę aplikacji logiki, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cde38-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde38-122">-ResourceGroupName</span></span>
<span data-ttu-id="cde38-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="cde38-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde38-124">— Wersja</span><span class="sxs-lookup"><span data-stu-id="cde38-124">-Version</span></span>
<span data-ttu-id="cde38-125">Określa wersję aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="cde38-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde38-126">CommonParameters</span></span>
<span data-ttu-id="cde38-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde38-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde38-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde38-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cde38-129">INPUTS</span></span>

### <span data-ttu-id="cde38-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cde38-130">System.String</span></span>

## <span data-ttu-id="cde38-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cde38-131">OUTPUTS</span></span>

### <span data-ttu-id="cde38-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="cde38-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="cde38-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="cde38-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="cde38-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cde38-134">NOTES</span></span>

## <span data-ttu-id="cde38-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cde38-135">RELATED LINKS</span></span>

[<span data-ttu-id="cde38-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cde38-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="cde38-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cde38-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="cde38-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cde38-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="cde38-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cde38-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



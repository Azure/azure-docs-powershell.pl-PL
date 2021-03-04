---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 98232807cc5f7624242cd44c7d27579ef0f92d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958698"
---
# <span data-ttu-id="26a15-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="26a15-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="26a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a15-102">SYNOPSIS</span></span>
<span data-ttu-id="26a15-103">Pobiera aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26a15-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="26a15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26a15-104">SYNTAX</span></span>

### <span data-ttu-id="26a15-105">ListWorkflows (Default)</span><span class="sxs-lookup"><span data-stu-id="26a15-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26a15-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="26a15-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26a15-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="26a15-107">DESCRIPTION</span></span>
<span data-ttu-id="26a15-108">Polecenie **cmdlet Get-AzLogicApp** pobiera aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="26a15-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="26a15-109">To polecenie cmdlet zwraca obiekt **przepływu** pracy.</span><span class="sxs-lookup"><span data-stu-id="26a15-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="26a15-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="26a15-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="26a15-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="26a15-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="26a15-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="26a15-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="26a15-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="26a15-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="26a15-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26a15-114">EXAMPLES</span></span>

### <span data-ttu-id="26a15-115">Przykład 1. Uzyskiwanie aplikacji logiki z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26a15-115">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="26a15-116">To polecenie pobiera aplikację logiczną z grupy zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="26a15-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="26a15-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26a15-117">PARAMETERS</span></span>

### <span data-ttu-id="26a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a15-118">-DefaultProfile</span></span>
<span data-ttu-id="26a15-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="26a15-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26a15-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26a15-120">-Name</span></span>
<span data-ttu-id="26a15-121">Określa nazwę aplikacji logiki, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a15-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26a15-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a15-122">-ResourceGroupName</span></span>
<span data-ttu-id="26a15-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="26a15-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="26a15-124">— Wersja</span><span class="sxs-lookup"><span data-stu-id="26a15-124">-Version</span></span>
<span data-ttu-id="26a15-125">Określa wersję aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="26a15-125">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="26a15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a15-126">CommonParameters</span></span>
<span data-ttu-id="26a15-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a15-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a15-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a15-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a15-129">INPUTS</span></span>

### <span data-ttu-id="26a15-130">System.String</span><span class="sxs-lookup"><span data-stu-id="26a15-130">System.String</span></span>

## <span data-ttu-id="26a15-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a15-131">OUTPUTS</span></span>

### <span data-ttu-id="26a15-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="26a15-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="26a15-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="26a15-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="26a15-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26a15-134">NOTES</span></span>

## <span data-ttu-id="26a15-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26a15-135">RELATED LINKS</span></span>

[<span data-ttu-id="26a15-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="26a15-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="26a15-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="26a15-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="26a15-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="26a15-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="26a15-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="26a15-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



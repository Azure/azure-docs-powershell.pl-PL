---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 740ef9b21a2e2caa839880ff2c5e9dadc042351a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552771"
---
# <span data-ttu-id="a06ef-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a06ef-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="a06ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a06ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a06ef-103">Pobiera aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a06ef-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a06ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a06ef-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a06ef-105">DESCRIPTION</span></span>
<span data-ttu-id="a06ef-106">Polecenie cmdlet **Get-AzureRmLogicApp** pobiera aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="a06ef-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="a06ef-107">To polecenie cmdlet zwraca obiekt **przepływu pracy** .</span><span class="sxs-lookup"><span data-stu-id="a06ef-107">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="a06ef-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a06ef-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a06ef-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="a06ef-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a06ef-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="a06ef-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a06ef-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="a06ef-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a06ef-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a06ef-112">EXAMPLES</span></span>

### <span data-ttu-id="a06ef-113">Przykład 1: uzyskiwanie aplikacji logicznej z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a06ef-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="a06ef-114">To polecenie pobiera aplikację logiczną z grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a06ef-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a06ef-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a06ef-115">PARAMETERS</span></span>

### <span data-ttu-id="a06ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06ef-116">-DefaultProfile</span></span>
<span data-ttu-id="a06ef-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a06ef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a06ef-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a06ef-118">-Name</span></span>
<span data-ttu-id="a06ef-119">Określa nazwę aplikacji logicznej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06ef-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="a06ef-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="a06ef-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="a06ef-122">-Version</span><span class="sxs-lookup"><span data-stu-id="a06ef-122">-Version</span></span>
<span data-ttu-id="a06ef-123">Określa wersję aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="a06ef-123">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="a06ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06ef-124">CommonParameters</span></span>
<span data-ttu-id="a06ef-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06ef-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06ef-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a06ef-127">INPUTS</span></span>

### <span data-ttu-id="a06ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a06ef-128">System.String</span></span>

## <span data-ttu-id="a06ef-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a06ef-129">OUTPUTS</span></span>

### <span data-ttu-id="a06ef-130">Microsoft. Azure. Management. Logic. models. Workflow</span><span class="sxs-lookup"><span data-stu-id="a06ef-130">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="a06ef-131">Microsoft. Azure. Management. Logic. MODELES. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="a06ef-131">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="a06ef-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a06ef-132">NOTES</span></span>

## <span data-ttu-id="a06ef-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a06ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="a06ef-134">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a06ef-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a06ef-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a06ef-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="a06ef-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a06ef-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a06ef-137">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a06ef-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



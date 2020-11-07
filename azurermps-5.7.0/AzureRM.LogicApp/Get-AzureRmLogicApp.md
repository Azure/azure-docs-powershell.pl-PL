---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 3faa9ce82806da0e2f058f3d1bcaeba3862c27c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717737"
---
# <span data-ttu-id="7864e-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7864e-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="7864e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7864e-102">SYNOPSIS</span></span>
<span data-ttu-id="7864e-103">Pobiera aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7864e-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7864e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7864e-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7864e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7864e-105">DESCRIPTION</span></span>
<span data-ttu-id="7864e-106">Polecenie cmdlet **Get-AzureRmLogicApp** pobiera aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="7864e-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="7864e-107">To polecenie cmdlet zwraca obiekt **przepływu pracy** .</span><span class="sxs-lookup"><span data-stu-id="7864e-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="7864e-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="7864e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7864e-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7864e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7864e-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7864e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7864e-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="7864e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7864e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7864e-112">EXAMPLES</span></span>

### <span data-ttu-id="7864e-113">Przykład 1: uzyskiwanie aplikacji logicznej z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7864e-113">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="7864e-114">To polecenie pobiera aplikację logiczną z grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7864e-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7864e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7864e-115">PARAMETERS</span></span>

### <span data-ttu-id="7864e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7864e-116">-DefaultProfile</span></span>
<span data-ttu-id="7864e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7864e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7864e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7864e-118">-Name</span></span>
<span data-ttu-id="7864e-119">Określa nazwę aplikacji logicznej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7864e-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7864e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7864e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7864e-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera aplikację logiczną.</span><span class="sxs-lookup"><span data-stu-id="7864e-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7864e-122">-Version</span><span class="sxs-lookup"><span data-stu-id="7864e-122">-Version</span></span>
<span data-ttu-id="7864e-123">Określa wersję aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="7864e-123">Specifies the version of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7864e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7864e-124">CommonParameters</span></span>
<span data-ttu-id="7864e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7864e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7864e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7864e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7864e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7864e-127">INPUTS</span></span>

### <span data-ttu-id="7864e-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7864e-128">None</span></span>
<span data-ttu-id="7864e-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7864e-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7864e-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7864e-130">OUTPUTS</span></span>

### <span data-ttu-id="7864e-131">Microsoft. Azure. Management. Logic. models. Workflow</span><span class="sxs-lookup"><span data-stu-id="7864e-131">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="7864e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7864e-132">NOTES</span></span>

## <span data-ttu-id="7864e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7864e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7864e-134">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7864e-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="7864e-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7864e-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="7864e-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7864e-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="7864e-137">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7864e-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



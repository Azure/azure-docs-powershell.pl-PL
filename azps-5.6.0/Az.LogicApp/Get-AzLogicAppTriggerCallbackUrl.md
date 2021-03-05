---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 10408574a36018293fd15ef4f258ef4923f21d8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008906"
---
# <span data-ttu-id="d36e2-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d36e2-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="d36e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d36e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d36e2-103">Pobiera adres URL wyzwalania wywołania zwrotnego aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="d36e2-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="d36e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d36e2-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d36e2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d36e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d36e2-106">Polecenie **cmdlet Get-AzLogicAppTriggerCallbackUrl** pobiera adres URL wyzwalany przez aplikację logic z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d36e2-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="d36e2-107">To polecenie cmdlet zwraca obiekt **WorkflowTriggerCallbackUrl** reprezentujący adres URL wywołania zwrotnego.</span><span class="sxs-lookup"><span data-stu-id="d36e2-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="d36e2-108">Określ nazwę grupy zasobów, nazwę aplikacji logiki i nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d36e2-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="d36e2-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="d36e2-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d36e2-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d36e2-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d36e2-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="d36e2-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d36e2-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="d36e2-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d36e2-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d36e2-113">EXAMPLES</span></span>

### <span data-ttu-id="d36e2-114">Przykład 1. Uzyskiwanie adresu URL wyzwalacza wywołania zwrotnego aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="d36e2-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="d36e2-115">To polecenie pobiera adres URL wyzwalacza wywołania zwrotnego aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="d36e2-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="d36e2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d36e2-116">PARAMETERS</span></span>

### <span data-ttu-id="d36e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36e2-117">-DefaultProfile</span></span>
<span data-ttu-id="d36e2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d36e2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d36e2-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d36e2-119">-Name</span></span>
<span data-ttu-id="d36e2-120">Określa nazwę aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="d36e2-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d36e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d36e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d36e2-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d36e2-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d36e2-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d36e2-123">-TriggerName</span></span>
<span data-ttu-id="d36e2-124">Określa nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d36e2-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="d36e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36e2-125">CommonParameters</span></span>
<span data-ttu-id="d36e2-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d36e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36e2-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36e2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36e2-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d36e2-128">INPUTS</span></span>

### <span data-ttu-id="d36e2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d36e2-129">System.String</span></span>

## <span data-ttu-id="d36e2-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d36e2-130">OUTPUTS</span></span>

### <span data-ttu-id="d36e2-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d36e2-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="d36e2-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d36e2-132">NOTES</span></span>

## <span data-ttu-id="d36e2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d36e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="d36e2-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d36e2-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952458"
---
# <span data-ttu-id="c4b7c-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4b7c-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="c4b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b7c-103">Uruchamia aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="c4b7c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c4b7c-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b7c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c4b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c4b7c-106">Polecenie **cmdlet Start-AzLogicApp** uruchamia aplikację logiczną przy użyciu funkcji aplikacje logic.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="c4b7c-107">Określanie nazwy, grupy zasobów i wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="c4b7c-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c4b7c-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c4b7c-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c4b7c-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c4b7c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c4b7c-112">EXAMPLES</span></span>

### <span data-ttu-id="c4b7c-113">Przykład 1. Uruchamianie aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="c4b7c-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="c4b7c-114">To polecenie uruchamia aplikację logiki w grupie zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c4b7c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4b7c-115">PARAMETERS</span></span>

### <span data-ttu-id="c4b7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b7c-116">-DefaultProfile</span></span>
<span data-ttu-id="c4b7c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c4b7c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4b7c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c4b7c-118">-Name</span></span>
<span data-ttu-id="c4b7c-119">Określa nazwę aplikacji logiki uruchamianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c4b7c-120">— Parametry</span><span class="sxs-lookup"><span data-stu-id="c4b7c-120">-Parameters</span></span>
<span data-ttu-id="c4b7c-121">Określa obiekt kolekcji parametrów aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="c4b7c-122">Określ tabelę skrótu, słownik \<string\> lub \<string, WorkflowParameter\> słownik.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="c4b7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4b7c-124">Określa nazwę grupy zasobów zawierającej aplikację logiczną uruchamianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c4b7c-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c4b7c-125">-TriggerName</span></span>
<span data-ttu-id="c4b7c-126">Określa nazwę wyzwalacza aplikacji logiki, które uruchamia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c4b7c-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4b7c-127">-Confirm</span></span>
<span data-ttu-id="c4b7c-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b7c-129">-WhatIf</span></span>
<span data-ttu-id="c4b7c-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b7c-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b7c-132">CommonParameters</span></span>
<span data-ttu-id="c4b7c-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b7c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b7c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b7c-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4b7c-135">INPUTS</span></span>

### <span data-ttu-id="c4b7c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c4b7c-136">System.String</span></span>

## <span data-ttu-id="c4b7c-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4b7c-137">OUTPUTS</span></span>

### <span data-ttu-id="c4b7c-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="c4b7c-138">System.Void</span></span>

## <span data-ttu-id="c4b7c-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c4b7c-139">NOTES</span></span>

## <span data-ttu-id="c4b7c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4b7c-140">RELATED LINKS</span></span>

[<span data-ttu-id="c4b7c-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4b7c-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="c4b7c-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c4b7c-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="c4b7c-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4b7c-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c4b7c-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4b7c-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c4b7c-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4b7c-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="c4b7c-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="c4b7c-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



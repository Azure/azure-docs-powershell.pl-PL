---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368342"
---
# <span data-ttu-id="52069-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="52069-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="52069-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52069-102">SYNOPSIS</span></span>
<span data-ttu-id="52069-103">Uruchamia aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="52069-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="52069-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52069-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52069-105">Opis</span><span class="sxs-lookup"><span data-stu-id="52069-105">DESCRIPTION</span></span>
<span data-ttu-id="52069-106">Polecenie cmdlet **Start-AzLogicApp** uruchamia aplikację logiczną za pomocą funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="52069-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="52069-107">Określ nazwę, grupę zasobów i wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="52069-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="52069-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="52069-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="52069-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="52069-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="52069-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="52069-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="52069-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="52069-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="52069-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52069-112">EXAMPLES</span></span>

### <span data-ttu-id="52069-113">Przykład 1. Uruchom aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="52069-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="52069-114">To polecenie uruchamia aplikację logiczną w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="52069-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="52069-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52069-115">PARAMETERS</span></span>

### <span data-ttu-id="52069-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52069-116">-DefaultProfile</span></span>
<span data-ttu-id="52069-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="52069-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52069-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52069-118">-Name</span></span>
<span data-ttu-id="52069-119">Określa nazwę aplikacji logicznej, która zostanie uruchomiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52069-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52069-120">— Parametry</span><span class="sxs-lookup"><span data-stu-id="52069-120">-Parameters</span></span>
<span data-ttu-id="52069-121">Określa obiekt kolekcji Parameters aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="52069-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="52069-122">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="52069-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="52069-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52069-123">-ResourceGroupName</span></span>
<span data-ttu-id="52069-124">Określa nazwę grupy zasobów zawierającej aplikację logiczną, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52069-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52069-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="52069-125">-TriggerName</span></span>
<span data-ttu-id="52069-126">Określa nazwę wyzwalacza aplikacji logicznej, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52069-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52069-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52069-127">-Confirm</span></span>
<span data-ttu-id="52069-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52069-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52069-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52069-129">-WhatIf</span></span>
<span data-ttu-id="52069-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52069-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52069-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52069-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52069-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52069-132">CommonParameters</span></span>
<span data-ttu-id="52069-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52069-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52069-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52069-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52069-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52069-135">INPUTS</span></span>

### <span data-ttu-id="52069-136">System. String</span><span class="sxs-lookup"><span data-stu-id="52069-136">System.String</span></span>

## <span data-ttu-id="52069-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52069-137">OUTPUTS</span></span>

### <span data-ttu-id="52069-138">System. void</span><span class="sxs-lookup"><span data-stu-id="52069-138">System.Void</span></span>

## <span data-ttu-id="52069-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52069-139">NOTES</span></span>

## <span data-ttu-id="52069-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52069-140">RELATED LINKS</span></span>

[<span data-ttu-id="52069-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="52069-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="52069-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="52069-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="52069-143">Nowe — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="52069-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="52069-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="52069-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="52069-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="52069-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="52069-146">Zatrzymaj — AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="52069-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719463"
---
# <span data-ttu-id="840e1-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="840e1-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="840e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="840e1-102">SYNOPSIS</span></span>
<span data-ttu-id="840e1-103">Uruchamia aplikację logiczną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="840e1-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="840e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="840e1-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="840e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="840e1-105">DESCRIPTION</span></span>
<span data-ttu-id="840e1-106">Polecenie cmdlet **Start-AzureRmLogicApp** uruchamia aplikację logiczną za pomocą funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="840e1-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="840e1-107">Określ nazwę, grupę zasobów i wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="840e1-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="840e1-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="840e1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="840e1-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="840e1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="840e1-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="840e1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="840e1-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="840e1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="840e1-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="840e1-112">EXAMPLES</span></span>

### <span data-ttu-id="840e1-113">Przykład 1. Uruchom aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="840e1-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="840e1-114">To polecenie uruchamia aplikację logiczną w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="840e1-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="840e1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="840e1-115">PARAMETERS</span></span>

### <span data-ttu-id="840e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840e1-116">-DefaultProfile</span></span>
<span data-ttu-id="840e1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="840e1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="840e1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="840e1-118">-Name</span></span>
<span data-ttu-id="840e1-119">Określa nazwę aplikacji logicznej, która zostanie uruchomiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840e1-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840e1-120">— Parametry</span><span class="sxs-lookup"><span data-stu-id="840e1-120">-Parameters</span></span>
<span data-ttu-id="840e1-121">Określa obiekt kolekcji Parameters aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="840e1-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="840e1-122">Określ tabelę skrótów, słownik \<string\> lub słownik \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="840e1-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="840e1-124">Określa nazwę grupy zasobów zawierającej aplikację logiczną, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840e1-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="840e1-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="840e1-125">-TriggerName</span></span>
<span data-ttu-id="840e1-126">Określa nazwę wyzwalacza aplikacji logicznej, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840e1-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="840e1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="840e1-127">-Confirm</span></span>
<span data-ttu-id="840e1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840e1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840e1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="840e1-129">-WhatIf</span></span>
<span data-ttu-id="840e1-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840e1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="840e1-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="840e1-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840e1-132">CommonParameters</span></span>
<span data-ttu-id="840e1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="840e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840e1-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840e1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840e1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="840e1-135">INPUTS</span></span>

### <span data-ttu-id="840e1-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="840e1-136">None</span></span>
<span data-ttu-id="840e1-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="840e1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="840e1-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="840e1-138">OUTPUTS</span></span>

### <span data-ttu-id="840e1-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="840e1-139">System.Object</span></span>

## <span data-ttu-id="840e1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="840e1-140">NOTES</span></span>

## <span data-ttu-id="840e1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="840e1-141">RELATED LINKS</span></span>

[<span data-ttu-id="840e1-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="840e1-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="840e1-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="840e1-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="840e1-144">Nowe — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="840e1-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="840e1-145">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="840e1-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="840e1-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="840e1-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="840e1-147">Zatrzymaj — AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="840e1-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)



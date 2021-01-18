---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500818"
---
# <span data-ttu-id="6960f-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6960f-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="6960f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6960f-102">SYNOPSIS</span></span>
<span data-ttu-id="6960f-103">Usuwa aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6960f-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="6960f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6960f-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6960f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6960f-105">DESCRIPTION</span></span>
<span data-ttu-id="6960f-106">Polecenie cmdlet **Remove-AzLogicApp** usuwa aplikację logiczną z grupy zasobów przy użyciu funkcji aplikacje logiczne.</span><span class="sxs-lookup"><span data-stu-id="6960f-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="6960f-107">Określ aplikację logiczną i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="6960f-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6960f-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="6960f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6960f-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="6960f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6960f-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="6960f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6960f-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="6960f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6960f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6960f-112">EXAMPLES</span></span>

### <span data-ttu-id="6960f-113">Przykład 1. Usuń aplikację logiczną</span><span class="sxs-lookup"><span data-stu-id="6960f-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="6960f-114">To polecenie usuwa aplikację logiczną z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6960f-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="6960f-115">Polecenie zawiera parametr *Force* , co zapobiegnie wyświetleniu przez polecenie monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6960f-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="6960f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6960f-116">PARAMETERS</span></span>

### <span data-ttu-id="6960f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6960f-117">-DefaultProfile</span></span>
<span data-ttu-id="6960f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6960f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6960f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6960f-119">-Force</span></span>
<span data-ttu-id="6960f-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6960f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6960f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6960f-121">-Name</span></span>
<span data-ttu-id="6960f-122">Określa nazwę aplikacji logicznej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6960f-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6960f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6960f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6960f-124">Określa nazwę grupy zasobów zawierającej aplikację logiczną, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6960f-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6960f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6960f-125">-Confirm</span></span>
<span data-ttu-id="6960f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6960f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6960f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6960f-127">-WhatIf</span></span>
<span data-ttu-id="6960f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6960f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6960f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6960f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6960f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6960f-130">CommonParameters</span></span>
<span data-ttu-id="6960f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6960f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6960f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6960f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6960f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6960f-133">INPUTS</span></span>

### <span data-ttu-id="6960f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6960f-134">System.String</span></span>

## <span data-ttu-id="6960f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6960f-135">OUTPUTS</span></span>

### <span data-ttu-id="6960f-136">System. void</span><span class="sxs-lookup"><span data-stu-id="6960f-136">System.Void</span></span>

## <span data-ttu-id="6960f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6960f-137">NOTES</span></span>

## <span data-ttu-id="6960f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6960f-138">RELATED LINKS</span></span>

[<span data-ttu-id="6960f-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6960f-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="6960f-140">Nowe — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6960f-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="6960f-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6960f-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="6960f-142">Start — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6960f-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



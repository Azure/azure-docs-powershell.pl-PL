---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233415"
---
# <span data-ttu-id="46427-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="46427-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="46427-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46427-102">SYNOPSIS</span></span>
<span data-ttu-id="46427-103">Anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="46427-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="46427-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46427-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46427-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46427-105">DESCRIPTION</span></span>
<span data-ttu-id="46427-106">Polecenie cmdlet **stop-AzLogicAppRun** anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="46427-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="46427-107">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="46427-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="46427-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="46427-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="46427-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="46427-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="46427-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="46427-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="46427-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="46427-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="46427-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46427-112">EXAMPLES</span></span>

### <span data-ttu-id="46427-113">Przykład 1. Anulowanie uruchomienia aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="46427-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="46427-114">To polecenie anuluje uruchomienie aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="46427-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="46427-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46427-115">PARAMETERS</span></span>

### <span data-ttu-id="46427-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46427-116">-DefaultProfile</span></span>
<span data-ttu-id="46427-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="46427-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46427-118">-Force</span><span class="sxs-lookup"><span data-stu-id="46427-118">-Force</span></span>
<span data-ttu-id="46427-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="46427-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46427-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46427-120">-Name</span></span>
<span data-ttu-id="46427-121">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="46427-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="46427-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46427-122">-ResourceGroupName</span></span>
<span data-ttu-id="46427-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="46427-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="46427-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="46427-124">-RunName</span></span>
<span data-ttu-id="46427-125">Określa nazwę aplikacji logicznej, za pomocą której anuluje się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46427-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="46427-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46427-126">-Confirm</span></span>
<span data-ttu-id="46427-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46427-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46427-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46427-128">-WhatIf</span></span>
<span data-ttu-id="46427-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46427-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46427-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46427-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46427-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46427-131">CommonParameters</span></span>
<span data-ttu-id="46427-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46427-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46427-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46427-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46427-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46427-134">INPUTS</span></span>

### <span data-ttu-id="46427-135">System. String</span><span class="sxs-lookup"><span data-stu-id="46427-135">System.String</span></span>

## <span data-ttu-id="46427-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46427-136">OUTPUTS</span></span>

### <span data-ttu-id="46427-137">System. void</span><span class="sxs-lookup"><span data-stu-id="46427-137">System.Void</span></span>

## <span data-ttu-id="46427-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46427-138">NOTES</span></span>

## <span data-ttu-id="46427-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46427-139">RELATED LINKS</span></span>

[<span data-ttu-id="46427-140">Start — AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="46427-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



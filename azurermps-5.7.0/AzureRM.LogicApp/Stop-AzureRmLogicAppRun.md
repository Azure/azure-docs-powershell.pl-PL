---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: 1d23c4f92a73a2ec6471169a05c1048d96abcaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545664"
---
# <span data-ttu-id="d32e6-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d32e6-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="d32e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d32e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d32e6-103">Anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="d32e6-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d32e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d32e6-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d32e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d32e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d32e6-106">Polecenie cmdlet **stop-AzureRmLogicAppRun** anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="d32e6-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="d32e6-107">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="d32e6-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="d32e6-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="d32e6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d32e6-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d32e6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d32e6-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="d32e6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d32e6-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="d32e6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d32e6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d32e6-112">EXAMPLES</span></span>

### <span data-ttu-id="d32e6-113">Przykład 1. Anulowanie uruchomienia aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="d32e6-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="d32e6-114">To polecenie anuluje uruchomienie aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="d32e6-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="d32e6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d32e6-115">PARAMETERS</span></span>

### <span data-ttu-id="d32e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32e6-116">-DefaultProfile</span></span>
<span data-ttu-id="d32e6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d32e6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d32e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d32e6-118">-Force</span></span>
<span data-ttu-id="d32e6-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d32e6-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32e6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d32e6-120">-Name</span></span>
<span data-ttu-id="d32e6-121">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="d32e6-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="d32e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d32e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d32e6-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="d32e6-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="d32e6-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="d32e6-124">-RunName</span></span>
<span data-ttu-id="d32e6-125">Określa nazwę aplikacji logicznej, za pomocą której anuluje się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="d32e6-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d32e6-126">-Confirm</span></span>
<span data-ttu-id="d32e6-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d32e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d32e6-128">-WhatIf</span></span>
<span data-ttu-id="d32e6-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d32e6-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d32e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d32e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32e6-131">CommonParameters</span></span>
<span data-ttu-id="d32e6-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d32e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32e6-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32e6-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d32e6-134">INPUTS</span></span>

### <span data-ttu-id="d32e6-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d32e6-135">None</span></span>
<span data-ttu-id="d32e6-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d32e6-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d32e6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d32e6-137">OUTPUTS</span></span>

### <span data-ttu-id="d32e6-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="d32e6-138">System.Object</span></span>

## <span data-ttu-id="d32e6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d32e6-139">NOTES</span></span>

## <span data-ttu-id="d32e6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d32e6-140">RELATED LINKS</span></span>

[<span data-ttu-id="d32e6-141">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d32e6-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



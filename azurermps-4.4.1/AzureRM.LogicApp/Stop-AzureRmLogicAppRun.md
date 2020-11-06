---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: c6c2c356557d2d9d40a4012a7deee5aec0e73aa4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554347"
---
# <span data-ttu-id="eef25-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="eef25-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="eef25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eef25-102">SYNOPSIS</span></span>
<span data-ttu-id="eef25-103">Anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="eef25-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eef25-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eef25-105">DESCRIPTION</span></span>
<span data-ttu-id="eef25-106">Polecenie cmdlet **stop-AzureRmLogicAppRun** anuluje uruchomienie aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="eef25-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="eef25-107">Określ aplikację logiczną, grupę zasobów i działanie.</span><span class="sxs-lookup"><span data-stu-id="eef25-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="eef25-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="eef25-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="eef25-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="eef25-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="eef25-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="eef25-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="eef25-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="eef25-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="eef25-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eef25-112">EXAMPLES</span></span>

### <span data-ttu-id="eef25-113">Przykład 1. Anulowanie uruchomienia aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="eef25-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="eef25-114">To polecenie anuluje uruchomienie aplikacji logicznej o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="eef25-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="eef25-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eef25-115">PARAMETERS</span></span>

### <span data-ttu-id="eef25-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eef25-116">-Force</span></span>
<span data-ttu-id="eef25-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="eef25-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eef25-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eef25-118">-Name</span></span>
<span data-ttu-id="eef25-119">Określa nazwę aplikacji logicznej, dla której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="eef25-119">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="eef25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef25-120">-ResourceGroupName</span></span>
<span data-ttu-id="eef25-121">Określa nazwę grupy zasobów, w której to polecenie cmdlet anuluje uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="eef25-121">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="eef25-122">-RunName</span><span class="sxs-lookup"><span data-stu-id="eef25-122">-RunName</span></span>
<span data-ttu-id="eef25-123">Określa nazwę aplikacji logicznej, za pomocą której anuluje się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eef25-123">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="eef25-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eef25-124">-Confirm</span></span>
<span data-ttu-id="eef25-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eef25-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef25-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef25-126">-WhatIf</span></span>
<span data-ttu-id="eef25-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eef25-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eef25-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eef25-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef25-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef25-129">-DefaultProfile</span></span>
<span data-ttu-id="eef25-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eef25-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef25-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef25-131">CommonParameters</span></span>
<span data-ttu-id="eef25-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef25-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef25-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef25-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef25-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eef25-134">INPUTS</span></span>

## <span data-ttu-id="eef25-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eef25-135">OUTPUTS</span></span>

### <span data-ttu-id="eef25-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="eef25-136">System.Object</span></span>

## <span data-ttu-id="eef25-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eef25-137">NOTES</span></span>

## <span data-ttu-id="eef25-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eef25-138">RELATED LINKS</span></span>

[<span data-ttu-id="eef25-139">Start — AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="eef25-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


